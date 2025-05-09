# Results vs. 3.12.6

- fork: python
- ref: 6d5a8c2ec19f1c38b455
- machine: darwin-arm64
- commit hash: 6d5a8c2
- commit date: 2025-05-09
- overall geometric mean: 1.085x faster
- HPT reliability: 96.56%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 25.7 ms: 1.12x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.8 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| tomli_loads          | 957 ms                                                   | 986 ms: 1.03x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| json_loads           | 10.9 us                                                  | 12.5 us: 1.16x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 5.24 ms: 1.23x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.36 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.82 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                   |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 771 us: 2.60x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.63 ms: 2.16x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.8 ms: 1.96x faster                                                   |
| mdp                              | 1.09 sec                                                 | 583 ms: 1.87x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 483 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.32x faster                                                   |
| deepcopy                         | 161 us                                                   | 125 us: 1.30x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 816 ns: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                   |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.29 us: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| go                               | 70.0 ms                                                  | 62.5 ms: 1.12x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.79 us: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.8 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.7 ms: 1.04x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.00 ms: 1.00x faster                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 146 ms: 1.03x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 986 ms: 1.03x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                   |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 75.3 us: 1.06x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                   |
| json                             | 1.93 ms                                                  | 2.07 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 123 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.08x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 719 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.25 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.09x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.85 us: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.11x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 25.7 ms: 1.12x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.15 us: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                    |
| json_loads                       | 10.9 us                                                  | 12.5 us: 1.16x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.36 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.82 ms: 1.20x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 5.24 ms: 1.23x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.24x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.32 ms: 1.27x slower                                                   |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 66.8 ms: 1.30x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 600 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 214 ns: 4.21x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-6d5a8c2-NOGIL/bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 96.56% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x