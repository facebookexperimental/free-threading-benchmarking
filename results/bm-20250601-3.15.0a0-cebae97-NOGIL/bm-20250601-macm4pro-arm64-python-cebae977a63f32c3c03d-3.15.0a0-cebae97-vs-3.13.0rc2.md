# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.006x faster
- HPT reliability: 84.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.2 ms: 1.50x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.1 ms: 1.16x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| nbody          | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.6 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| mako            | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 797 us: 2.56x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 497 us: 2.00x faster                                                    |
| mdp                              | 1.06 sec                                                       | 566 ms: 1.87x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.2 ms: 1.50x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.17x faster                                                   |
| go                               | 72.6 ms                                                        | 62.1 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.1 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.6 ms: 1.04x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.05 ms: 1.07x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.32 ms: 1.08x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.09 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.3 ms: 1.11x slower                                                   |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.6 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 28.0 ms: 1.14x slower                                                   |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.1 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.00 us: 1.18x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.6 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 384 ms: 1.19x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 780 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.7 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.85 us: 1.28x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.16 us: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.5 ms: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 593 us: 1.44x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 64.3 ms: 1.50x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.87 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 219 ns: 5.40x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): tomli_loads, pidigits
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 84.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x