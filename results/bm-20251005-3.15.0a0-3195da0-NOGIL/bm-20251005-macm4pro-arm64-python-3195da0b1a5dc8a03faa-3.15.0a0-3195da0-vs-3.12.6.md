# Results vs. 3.12.6

- fork: python
- ref: 3195da0b1a5dc8a03faa
- machine: darwin-arm64
- commit hash: 3195da0
- commit date: 2025-10-05
- overall geometric mean: 1.080x faster
- HPT reliability: 94.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.1 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.49 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.7 ms: 1.16x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.02 ms: 1.06x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 976 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| mako            | 4.77 ms                                                  | 5.79 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 774 us: 2.60x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.1 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 609 ms: 1.79x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 481 us: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.38x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| float                            | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 832 ns: 1.16x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.47 us: 1.16x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.7 ms: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| go                               | 70.0 ms                                                  | 62.3 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 999 ms: 1.12x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.6 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 134 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 19.4 ms: 1.07x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.02 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 52.2 ms: 1.04x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 137 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.49 ms: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.00x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 43.7 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 976 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                   |
| chaos                            | 28.9 ms                                                  | 30.0 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                   |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.8 us: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.1 ms: 1.06x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.4 ms: 1.07x slower                                                   |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.4 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 354 ms: 1.08x slower                                                    |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 723 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.2 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.2 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.2 ms: 1.18x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.79 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 555 us: 1.33x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.5 ms: 1.51x slower                                                   |
| many_optionals                   | 195 us                                                   | 347 us: 1.78x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): logging_format, async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 94.76% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x