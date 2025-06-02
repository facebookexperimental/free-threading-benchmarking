# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.018x faster
- HPT reliability: 62.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 415 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.58x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.7 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 926 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.3 ms: 1.06x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.9 us: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.90 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.93 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 514 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.58x faster                                                    |
| k_core                           | 1.46 sec                                                       | 951 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.4 ms: 1.27x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.27x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| go                               | 72.6 ms                                                        | 58.4 ms: 1.24x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 926 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.3 ms: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 948 us: 1.05x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.9 us: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 203 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.90 ms: 1.01x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.9 us: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 960 ns: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                   |
| sphinx                           | 409 ms                                                         | 415 ms: 1.01x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.3 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.5 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 503 ms: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.0 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.8 ms: 1.09x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.51 us: 1.10x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.93 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 360 ms: 1.12x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 728 ms: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.3 ms: 1.13x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.1 ms: 1.13x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.80 us: 1.14x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.59 us: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.25x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.67 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.7 ms: 3.07x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 197 ns: 4.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (4): scimark_monte_carlo, async_tree_eager_cpu_io_mixed, sympy_integrate, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.018x faster

# HPT report

- Reliability score: 62.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x