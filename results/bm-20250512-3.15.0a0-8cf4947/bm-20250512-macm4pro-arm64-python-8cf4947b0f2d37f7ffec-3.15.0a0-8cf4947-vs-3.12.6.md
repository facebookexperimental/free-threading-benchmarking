# Results vs. 3.12.6

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: darwin-arm64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.086x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 26.6 ms: 1.15x slower                                                   |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 51.1 ms: 1.06x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.57 ms: 1.06x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 103 ms: 1.03x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.6 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.01x faster                                                    |
| tomli_loads          | 957 ms                                                   | 964 ms: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.08x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 5.23 ms: 1.23x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 4.84 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.82 ms: 2.12x faster                                                   |
| mdp                              | 1.09 sec                                                 | 536 ms: 2.04x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                   |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.81 us: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| float                            | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.7 ms: 1.18x faster                                                   |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 965 ms: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.6 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.1 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.08x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.57 ms: 1.06x faster                                                   |
| nbody                            | 54.2 ms                                                  | 51.1 ms: 1.06x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 67.0 us: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.7 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 305 us: 1.05x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.64 ms: 1.05x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.01 ms: 1.03x faster                                                   |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 949 ns: 1.02x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.2 ms: 1.01x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.3 ms: 1.00x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 964 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.84 ms: 1.01x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.85 us: 1.02x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 103 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.05x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 51.2 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 26.6 ms: 1.15x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 960 us: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                   |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 5.23 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.73x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 194 ns: 3.82x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (5): richards, pprint_pformat, pprint_safe_repr, connected_components, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x