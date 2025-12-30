# Results vs. 3.13.0rc2

- fork: python
- ref: b6b0e14b3d4aa9e9b89b
- machine: darwin-arm64
- commit hash: b6b0e14
- commit date: 2025-12-29
- overall geometric mean: 1.002x faster
- HPT reliability: 81.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.06 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.0 ms: 1.16x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.26 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                    |
| mako            | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 822 us: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 522 us: 1.90x faster                                                     |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.14 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 999 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.3 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.4 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 4.06 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 831 ns: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 124 ms: 1.01x slower                                                     |
| tomli_loads                      | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 334 ms: 1.04x slower                                                     |
| json                             | 1.94 ms                                                        | 2.02 ms: 1.04x slower                                                    |
| sphinx                           | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 684 ms: 1.05x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.17 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 338 us: 1.09x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.5 us: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.76 us: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                     |
| pylint                           | 106 ms                                                         | 121 ms: 1.14x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.0 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.0 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 57.1 ms: 1.19x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.14 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.26 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.31 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.4 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.6 ms: 1.27x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 547 us: 1.33x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.9 ms: 1.33x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 273 us: 1.36x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 58.7 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 81.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x