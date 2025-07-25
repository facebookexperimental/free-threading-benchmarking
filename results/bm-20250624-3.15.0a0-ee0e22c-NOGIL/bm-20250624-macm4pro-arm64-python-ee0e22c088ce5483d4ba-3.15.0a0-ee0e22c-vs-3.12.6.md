# Results vs. 3.12.6

- fork: python
- ref: ee0e22c088ce5483d4ba
- machine: darwin-arm64
- commit hash: ee0e22c
- commit date: 2025-06-24
- overall geometric mean: 1.100x faster
- HPT reliability: 98.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.1 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.0 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.3 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| tomli_loads          | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.97 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                   |
| django_template | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 790 us: 2.54x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.76 ms: 2.13x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| mdp                              | 1.09 sec                                                 | 569 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 494 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.88 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 831 ns: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.5 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 130 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.4 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.2 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.6 ms: 1.05x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.0 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.02x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.00 ms: 1.01x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 98.3 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                    |
| thrift                           | 322 us                                                   | 330 us: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.0 us: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 343 ms: 1.05x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 700 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.06x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 55.1 ms: 1.07x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.1 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                   |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.81 us: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.14 us: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.1 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.97 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.19 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 257 us: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 599 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 219 ns: 4.31x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): sympy_integrate, nbody
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 98.70% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x