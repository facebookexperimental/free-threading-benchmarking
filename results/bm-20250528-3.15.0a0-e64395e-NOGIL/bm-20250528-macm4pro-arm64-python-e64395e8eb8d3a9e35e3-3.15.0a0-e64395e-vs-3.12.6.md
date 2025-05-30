# Results vs. 3.12.6

- fork: python
- ref: e64395e8eb8d3a9e35e3
- machine: darwin-arm64
- commit hash: e64395e
- commit date: 2025-05-28
- overall geometric mean: 1.096x faster
- HPT reliability: 99.21%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 995 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.9 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.58 ms: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.10x slower                                                    |
| json_loads           | 10.9 us                                                  | 12.4 us: 1.15x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.40 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 762 us: 2.64x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.80 ms: 2.12x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.9 ms: 1.96x faster                                                   |
| mdp                              | 1.09 sec                                                 | 565 ms: 1.93x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 473 us: 1.75x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.90 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| go                               | 70.0 ms                                                  | 60.4 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 839 ns: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 983 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.9 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.4 ms: 1.08x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.9 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 469 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 995 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.89 ms: 1.02x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 3.01 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.9 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 333 us: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.1 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                   |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.07x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.58 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.80 us: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.10x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.11 us: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.8 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                    |
| json_loads                       | 10.9 us                                                  | 12.4 us: 1.15x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 376 ms: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 769 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.40 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.31 ms: 1.27x slower                                                   |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 69.3 ms: 1.35x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 592 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 218 ns: 4.28x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): pidigits, nbody
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250528-3.15.0a0-e64395e-NOGIL/bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 99.21% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x