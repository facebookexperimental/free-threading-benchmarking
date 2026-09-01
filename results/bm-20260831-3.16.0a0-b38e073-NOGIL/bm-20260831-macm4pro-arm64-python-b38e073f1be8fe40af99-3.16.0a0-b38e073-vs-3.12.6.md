# Results vs. 3.12.6

- fork: python
- ref: b38e073f1be8fe40af99
- machine: darwin-arm64
- commit hash: b38e073
- commit date: 2026-08-31
- overall geometric mean: 1.013x faster
- HPT reliability: 68.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 461 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 312 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 314 ms: 1.53x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 309 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 163 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 187 ms: 1.23x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 150 ms: 1.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 148 ms: 1.17x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 303 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 309 ms: 1.08x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.0 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 51.9 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 281 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| nbody          | 54.2 ms                                                  | 63.7 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 68.8 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.1 ms: 1.03x faster                                                   |
| tomli_loads          | 957 ms                                                   | 943 ms: 1.01x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 39.3 ms: 1.01x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 118 us: 1.14x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 164 us: 1.18x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.7 ms: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.30x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.85 ms: 1.23x slower                                                   |
| django_template | 13.6 ms                                                  | 17.9 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.27x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.63 ms: 4.49x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 780 us: 2.57x faster                                                    |
| pylint                           | 128 ms                                                   | 54.3 ms: 2.36x faster                                                   |
| mdp                              | 1.09 sec                                                 | 621 ms: 1.76x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 492 us: 1.69x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 312 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 314 ms: 1.53x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 309 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| async_generators                 | 206 ms                                                   | 163 ms: 1.26x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 187 ms: 1.23x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 150 ms: 1.19x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 15.4 us: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 148 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.2 us: 1.16x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 303 ms: 1.12x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.82 us: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 309 ms: 1.08x faster                                                    |
| float                            | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.9 ms: 1.07x faster                                                   |
| go                               | 70.0 ms                                                  | 66.3 ms: 1.06x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.0 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.1 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 49.8 ns: 1.02x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 943 ms: 1.01x faster                                                    |
| pyflate                          | 216 ms                                                   | 214 ms: 1.01x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 60.8 ms: 1.00x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 39.3 ms: 1.01x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 508 ms: 1.02x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 44.5 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.66 us: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.93 us: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.50 ms: 1.06x slower                                                   |
| sphinx                           | 434 ms                                                   | 461 ms: 1.06x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                  |
| raytrace                         | 145 ms                                                   | 156 ms: 1.08x slower                                                    |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 62.1 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.1 ms: 1.09x slower                                                   |
| chaos                            | 28.9 ms                                                  | 31.7 ms: 1.09x slower                                                   |
| thrift                           | 322 us                                                   | 354 us: 1.10x slower                                                    |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 368 ms: 1.12x slower                                                    |
| generators                       | 21.9 ms                                                  | 24.8 ms: 1.13x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 757 ms: 1.14x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 51.9 ms: 1.14x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 118 us: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.8 ms: 1.15x slower                                                   |
| shortest_path                    | 219 ms                                                   | 254 ms: 1.16x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 194 ms: 1.16x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.55 ms: 1.17x slower                                                   |
| nbody                            | 54.2 ms                                                  | 63.7 ms: 1.17x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 164 us: 1.18x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.7 ms: 1.18x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                   |
| richards                         | 22.4 ms                                                  | 26.9 ms: 1.20x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 30.5 ms: 1.20x slower                                                   |
| 2to3                             | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.22x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.85 ms: 1.23x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 2.12 ms: 1.23x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 68.8 ms: 1.26x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.9 ms: 1.32x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 281 ms: 1.32x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 69.1 ms: 1.35x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 581 us: 1.39x slower                                                    |
| many_optionals                   | 195 us                                                   | 273 us: 1.40x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.5 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260831-3.16.0a0-b38e073-NOGIL/bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 68.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.33x