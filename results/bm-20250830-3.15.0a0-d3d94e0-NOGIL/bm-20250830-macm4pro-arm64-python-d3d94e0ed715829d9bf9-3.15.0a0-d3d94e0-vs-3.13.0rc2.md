# Results vs. 3.13.0rc2

- fork: python
- ref: d3d94e0ed715829d9bf9
- machine: darwin-arm64
- commit hash: d3d94e0
- commit date: 2025-08-30
- overall geometric mean: 1.000x faster
- HPT reliability: 82.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.02x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.4 ms: 1.23x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 972 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.07x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.78 ms: 1.13x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.06 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| mako            | 4.41 ms                                                        | 5.86 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 793 us: 2.58x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 499 us: 1.99x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 594 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.4 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.2 us: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| go                               | 72.6 ms                                                        | 62.8 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 827 ns: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                   |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 972 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| dask                             | 525 ms                                                         | 533 ms: 1.02x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.07x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 347 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.12 ms: 1.08x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                   |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.78 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| pylint                           | 106 ms                                                         | 120 ms: 1.13x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.14x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 46.1 ns: 1.14x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 74.5 us: 1.15x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 144 ms: 1.16x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.85 us: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.6 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.06 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.3 ms: 1.23x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.9 ms: 1.23x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.38 us: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.29 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.86 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.5 ms: 1.34x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 592 us: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 334 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.4 ms: 2.94x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250830-3.15.0a0-d3d94e0-NOGIL/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 82.42% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x