# Results vs. 3.13.0rc2

- fork: python
- ref: d3d94e0ed715829d9bf9
- machine: darwin-arm64
- commit hash: d3d94e0
- commit date: 2025-08-30
- overall geometric mean: 1.050x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.3 ms: 2.95x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 44.0 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 11.3 ms: 1.05x slower                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.74 ms: 1.08x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 106 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 786 ms: 1.27x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.2 ms: 1.09x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.5 us: 1.08x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 66.4 ms: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.02 ms: 1.11x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| mako            | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.1 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 523 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 954 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 50.9 ms: 1.43x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 786 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                   |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.1 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.02 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.10x faster                                                   |
| generators                       | 15.7 ms                                                        | 14.3 ms: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.2 ms: 1.09x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 44.0 ms: 1.09x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 92.5 us: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| thrift                           | 309 us                                                         | 292 us: 1.06x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 946 us: 1.05x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 38.8 ns: 1.05x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.14 us: 1.04x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 309 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 627 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.28 ms: 1.03x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 410 us: 1.00x faster                                                    |
| sympy_expand                     | 159 ms                                                         | 159 ms: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| meteor_contest                   | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.6 ms: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 482 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.04 us: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.6 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                    |
| regex_v8                         | 10.7 ms                                                        | 11.3 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.06x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.2 ms: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.4 ms: 1.06x slower                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.74 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 106 ms: 1.13x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.1 ms: 1.13x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.02 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 309 us: 1.54x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 16.7 ms: 2.67x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.3 ms: 2.95x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (6): json, sphinx, dask, sympy_str, python_startup, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250830-3.15.0a0-d3d94e0-CLANG/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x