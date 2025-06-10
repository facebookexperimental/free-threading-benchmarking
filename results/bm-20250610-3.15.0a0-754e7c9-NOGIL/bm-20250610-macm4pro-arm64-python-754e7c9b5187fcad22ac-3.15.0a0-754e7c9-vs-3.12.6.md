# Results vs. 3.12.6

- fork: python
- ref: 754e7c9b5187fcad22ac
- machine: darwin-arm64
- commit hash: 754e7c9
- commit date: 2025-06-10
- overall geometric mean: 1.095x faster
- HPT reliability: 98.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 998 ms: 1.02x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.3 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.8 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 985 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.56 ms: 1.07x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.43 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.66 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.59x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.69 ms: 2.14x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.3 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 563 ms: 1.94x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 486 us: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.32x faster                                                   |
| deepcopy                         | 161 us                                                   | 122 us: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.90 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 826 ns: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| go                               | 70.0 ms                                                  | 61.6 ms: 1.14x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 130 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.0 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.9 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.8 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 998 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.98 ms: 1.00x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 985 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.2 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.56 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.25 ms: 1.08x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.4 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.81 us: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.8 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.12 us: 1.11x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.6 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 379 ms: 1.16x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 774 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.43 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.66 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 62.1 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.20 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 251 us: 1.28x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 597 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250610-3.15.0a0-754e7c9-NOGIL/bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 98.14% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x