# Results vs. 3.12.6

- fork: python
- ref: f5dd52df16e1b3f3f8cc
- machine: darwin-arm64
- commit hash: f5dd52d
- commit date: 2026-09-11
- overall geometric mean: 1.002x faster
- HPT reliability: 85.26%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 138 ms: 1.21x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 463 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 318 ms: 1.56x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 309 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 323 ms: 1.42x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 302 ms: 1.12x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 203 ms: 1.10x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 164 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 313 ms: 1.07x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.8 ms: 1.06x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 264 ms: 1.14x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 151 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 283 ms: 1.33x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 167 ms: 1.48x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 71.5 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 120 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 62.4 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.36 ms: 1.23x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 69.9 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.0 ms: 1.23x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.1 ms: 1.13x faster                                                   |
| tomli_loads          | 957 ms                                                   | 968 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 40.1 ms: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 117 us: 1.14x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 164 us: 1.18x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.6 ms: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.30x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.91 ms: 1.24x slower                                                   |
| django_template | 13.6 ms                                                  | 18.1 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.28x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.67 ms: 4.44x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 774 us: 2.60x faster                                                    |
| pylint                           | 128 ms                                                   | 54.7 ms: 2.34x faster                                                   |
| mdp                              | 1.09 sec                                                 | 633 ms: 1.73x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 485 us: 1.71x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 318 ms: 1.56x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 309 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 323 ms: 1.42x faster                                                    |
| deepcopy                         | 161 us                                                   | 122 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.36 ms: 1.23x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.0 ms: 1.23x faster                                                   |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 812 ns: 1.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 60.9 us: 1.17x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 15.7 us: 1.16x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.1 ms: 1.13x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 302 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                  |
| comprehensions                   | 9.84 us                                                  | 8.90 us: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 203 ms: 1.10x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 164 ms: 1.08x faster                                                    |
| float                            | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 313 ms: 1.07x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.8 ms: 1.06x faster                                                   |
| go                               | 70.0 ms                                                  | 67.1 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| pyflate                          | 216 ms                                                   | 211 ms: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 501 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 968 ms: 1.01x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 62.0 ms: 1.02x slower                                                   |
| raytrace                         | 145 ms                                                   | 148 ms: 1.02x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 44.4 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 40.1 ms: 1.03x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.66 us: 1.04x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.93 us: 1.05x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 53.3 ns: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.06x slower                                                   |
| chaos                            | 28.9 ms                                                  | 30.8 ms: 1.06x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.56 ms: 1.07x slower                                                   |
| sphinx                           | 434 ms                                                   | 463 ms: 1.07x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                  |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 63.7 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 43.1 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 36.0 ms: 1.12x slower                                                   |
| sympy_str                        | 104 ms                                                   | 117 ms: 1.12x slower                                                    |
| thrift                           | 322 us                                                   | 364 us: 1.13x slower                                                    |
| generators                       | 21.9 ms                                                  | 24.9 ms: 1.14x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 117 us: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.4 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 264 ms: 1.14x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 151 ms: 1.15x slower                                                    |
| nbody                            | 54.2 ms                                                  | 62.4 ms: 1.15x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 378 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 256 ms: 1.17x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 780 ms: 1.17x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 164 us: 1.18x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.6 ms: 1.18x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.59 ms: 1.18x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 2.04 ms: 1.18x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 198 ms: 1.19x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.11 ms: 1.19x slower                                                   |
| richards                         | 22.4 ms                                                  | 26.9 ms: 1.20x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 30.5 ms: 1.20x slower                                                   |
| 2to3                             | 114 ms                                                   | 138 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.91 ms: 1.24x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 69.9 ms: 1.28x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                   |
| django_template                  | 13.6 ms                                                  | 18.1 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 283 ms: 1.33x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 69.7 ms: 1.36x slower                                                   |
| many_optionals                   | 195 us                                                   | 275 us: 1.41x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 167 ms: 1.48x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.7 ms: 1.51x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 71.5 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 120 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.00x slower                                                            |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 85.26% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x