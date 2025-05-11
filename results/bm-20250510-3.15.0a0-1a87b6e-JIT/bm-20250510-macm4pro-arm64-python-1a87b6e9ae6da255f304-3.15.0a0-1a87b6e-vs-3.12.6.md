# Results vs. 3.12.6

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 26.1 ms: 1.14x slower                                                   |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.2 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.0 ms: 1.09x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.55 ms: 1.07x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 101 ms: 1.01x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                   |
| tomli_loads          | 957 ms                                                   | 865 ms: 1.11x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 94.3 us: 1.09x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.5 ms: 1.07x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.9 us: 1.10x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 5.14 ms: 1.21x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.55 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.11 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.39 ms: 1.09x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.02x faster                                                   |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.38 ms: 2.21x faster                                                   |
| mdp                              | 1.09 sec                                                 | 540 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.48x faster                                                   |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.86 us: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 57.2 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 52.0 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 48.3 ms: 1.12x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 591 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 292 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 38.9 ms: 1.12x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 865 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 94.3 us: 1.09x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.39 ms: 1.09x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.0 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.55 ms: 1.07x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 66.3 us: 1.07x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.5 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.4 ms: 1.06x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.6 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.74 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.7 ms: 1.03x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 946 ns: 1.02x faster                                                    |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.8 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.4 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.09 ms: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 176 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 101 ms: 1.01x slower                                                    |
| pycparser                        | 497 ms                                                   | 504 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.02x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.61 us: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.87 us: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                   |
| shortest_path                    | 219 ms                                                   | 230 ms: 1.05x slower                                                    |
| connected_components             | 201 ms                                                   | 212 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.5 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.55 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.11 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 935 us: 1.13x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 26.1 ms: 1.14x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.14 ms: 1.21x slower                                                   |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.2 ms: 2.71x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 199 ns: 3.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): genshi_xml, asyncio_websockets
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.16x