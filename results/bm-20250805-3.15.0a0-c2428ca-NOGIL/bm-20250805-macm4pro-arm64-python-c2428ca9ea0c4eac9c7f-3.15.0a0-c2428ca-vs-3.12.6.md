# Results vs. 3.12.6

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: darwin-arm64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.082x faster
- HPT reliability: 95.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.6 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.4 ms: 1.04x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| nbody          | 54.2 ms                                                  | 61.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 1.01 sec: 1.06x slower                                                  |
| json_dumps           | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.97 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.62x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.6 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                    |
| mdp                              | 1.09 sec                                                 | 599 ms: 1.82x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 480 us: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.24 us: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.1 ns: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| go                               | 70.0 ms                                                  | 61.6 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.13x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.3 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 56.1 ms: 1.09x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.9 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.7 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.84 us: 1.01x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.02x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.3 us: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 335 us: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.4 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.06x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 1.01 sec: 1.06x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 726 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.27 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                   |
| nbody                            | 54.2 ms                                                  | 61.2 ms: 1.13x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 58.0 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.4 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.97 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.25 ms: 1.25x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 600 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 331 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (3): logging_simple, xml_etree_process, sympy_integrate
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 95.37% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x