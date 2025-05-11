# Results vs. 3.13.0rc2

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.003x faster
- HPT reliability: 77.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 25.9 ms: 1.12x slower                                                   |
| sphinx         | 409 ms                                                         | 420 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.17x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 986 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.5 ms: 1.09x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.27 ms: 1.13x slower                                                   |
| json_loads           | 10.8 us                                                        | 12.6 us: 1.17x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.39 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 778 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 482 us: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 579 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                    |
| go                               | 72.6 ms                                                        | 62.9 ms: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.4 us: 1.15x faster                                                   |
| deepcopy                         | 145 us                                                         | 127 us: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.9 ms: 1.12x faster                                                   |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| pyflate                          | 222 ms                                                         | 201 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 986 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 420 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.00 ms: 1.06x slower                                                   |
| json                             | 1.94 ms                                                        | 2.09 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.5 ms: 1.09x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.39 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.38 ms: 1.10x slower                                                   |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.12x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 359 ms: 1.12x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 726 ms: 1.12x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 25.9 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.13x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 5.27 ms: 1.13x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.17x slower                                                   |
| json_loads                       | 10.8 us                                                        | 12.6 us: 1.17x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 76.0 us: 1.18x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.6 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 30.0 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                   |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.85 us: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.13 us: 1.28x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.81 us: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.34x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 595 us: 1.44x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.68 ms: 1.55x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 67.0 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 217 ns: 5.34x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): deepcopy_reduce
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250510-3.15.0a0-1a87b6e-NOGIL/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 77.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x