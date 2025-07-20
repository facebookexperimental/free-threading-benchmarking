# Results vs. 3.12.6

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.143x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.95x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.63x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.55x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 38.6 ms: 1.18x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.2 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.9 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 170 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 104 ms: 1.05x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 806 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.1 ms: 1.16x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 45.0 ms: 1.15x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.04x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.31 ms: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.09 ms: 1.15x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.4 ms: 1.12x faster                                                   |
| mako            | 4.77 ms                                                  | 4.52 ms: 1.06x faster                                                   |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.08x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.49 ms: 2.19x faster                                                   |
| mdp                              | 1.09 sec                                                 | 509 ms: 2.14x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.95x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 99.8 us: 1.62x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.61x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.55x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.3 ms: 1.53x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.98 us: 1.41x faster                                                   |
| go                               | 70.0 ms                                                  | 50.8 ms: 1.38x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 38.5 ns: 1.32x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.3 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                   |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.54 ms: 1.20x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 59.6 us: 1.19x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 806 ms: 1.19x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 46.0 ms: 1.18x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 38.6 ms: 1.18x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| richards                         | 22.4 ms                                                  | 19.3 ms: 1.16x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.1 ms: 1.16x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.09 ms: 1.15x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.0 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.0 ms: 1.15x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.13x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.9 ms: 1.13x faster                                                   |
| thrift                           | 322 us                                                   | 284 us: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.4 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| sympy_str                        | 104 ms                                                   | 94.8 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.31 ms: 1.10x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.8 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 619 ms: 1.07x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.6 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.95 ms: 1.07x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 157 ms: 1.06x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.52 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 946 ns: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.0 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.31 ms: 1.01x slower                                                   |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 104 ms: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 170 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.14 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 997 us: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.2 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (2): json_loads, bench_thread_pool
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f-CLANG/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.143x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.13x