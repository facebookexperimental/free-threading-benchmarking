# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.059x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                   |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.5 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.97x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 43.4 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 816 ms: 1.23x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.32 ms: 1.08x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 93.9 us: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.2 ms: 1.11x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.09 ms: 1.10x faster                                                   |
| mako            | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                   |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| mdp                              | 1.06 sec                                                       | 507 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| k_core                           | 1.46 sec                                                       | 957 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.48x faster                                                   |
| deepcopy                         | 145 us                                                         | 98.6 us: 1.47x faster                                                   |
| go                               | 72.6 ms                                                        | 50.9 ms: 1.43x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.3 ms: 1.25x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 816 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                   |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.2 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.52 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                   |
| richards                         | 22.1 ms                                                        | 19.9 ms: 1.11x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.2 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.4 ms: 1.11x faster                                                   |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| richards_super                   | 24.7 ms                                                        | 22.4 ms: 1.10x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.09 ms: 1.10x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 58.9 us: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.5 ms: 1.09x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                   |
| thrift                           | 309 us                                                         | 286 us: 1.08x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.32 ms: 1.08x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.08x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 93.9 us: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 949 us: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.27 ms: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 93.9 ms: 1.02x faster                                                   |
| sympy_expand                     | 159 ms                                                         | 157 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 416 us: 1.01x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.1 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 477 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.99 us: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.0 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 45.5 ms: 1.06x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 48.5 ms: 1.11x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.13x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 237 us: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.28 ms: 1.48x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.97x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 193 ns: 4.76x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (3): sqlite_synth, dask, asyncio_websockets
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250601-3.15.0a0-cebae97-CLANG/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x