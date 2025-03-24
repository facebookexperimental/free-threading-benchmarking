# Results vs. 3.12.6

- fork: Yhg1s
- ref: uniqref_critsection
- machine: darwin-arm64
- commit hash: 60f2173
- commit date: 2025-03-24
- overall geometric mean: 1.015x slower
- HPT reliability: 99.44%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 130 ms: 1.14x slower                                                   |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                 |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                  |
| sphinx         | 434 ms                                                   | 439 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.13x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 234 ms: 2.12x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 99.4 ms: 1.73x faster                                                  |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.7 ms: 1.16x faster                                                  |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                   |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 55.6 ms: 1.22x slower                                                  |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                  |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.6 ms: 1.06x faster                                                  |
| nbody          | 54.2 ms                                                  | 78.8 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                    | 1.11x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                  |
| regex_dna      | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                  |
| regex_compile  | 54.6 ms                                                  | 59.4 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                    | 1.04x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.1 ms: 1.26x faster                                                  |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                  |
| xml_etree_generate   | 38.9 ms                                                  | 40.8 ms: 1.05x slower                                                  |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                  |
| xml_etree_process    | 26.7 ms                                                  | 30.5 ms: 1.14x slower                                                  |
| tomli_loads          | 957 ms                                                   | 1.09 sec: 1.14x slower                                                 |
| json_dumps           | 4.26 ms                                                  | 5.20 ms: 1.22x slower                                                  |
| pickle_pure_python   | 139 us                                                   | 171 us: 1.23x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.25x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.21 ms: 1.15x slower                                                  |
| python_startup_no_site | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                  |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.2 ms: 1.20x slower                                                  |
| genshi_text     | 10.5 ms                                                  | 13.1 ms: 1.25x slower                                                  |
| mako            | 4.77 ms                                                  | 6.23 ms: 1.31x slower                                                  |
| django_template | 13.6 ms                                                  | 18.2 ms: 1.33x slower                                                  |
| Geometric mean  | (ref)                                                    | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.21 ms: 2.25x faster                                                  |
| gc_traversal                     | 2.01 ms                                                  | 930 us: 2.16x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.13x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 234 ms: 2.12x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 99.4 ms: 1.73x faster                                                  |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 500 us: 1.66x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.1 ms: 1.26x faster                                                  |
| deepcopy                         | 161 us                                                   | 129 us: 1.25x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                  |
| coroutines                       | 13.6 ms                                                  | 11.7 ms: 1.16x faster                                                  |
| sqlite_synth                     | 967 ns                                                   | 842 ns: 1.15x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.7 ms: 1.08x faster                                                  |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                  |
| float                            | 37.9 ms                                                  | 35.6 ms: 1.06x faster                                                  |
| deepcopy_reduce                  | 1.46 us                                                  | 1.38 us: 1.06x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.8 ms: 1.05x faster                                                  |
| k_core                           | 1.12 sec                                                 | 1.07 sec: 1.05x faster                                                 |
| deepcopy_memo                    | 18.3 us                                                  | 17.6 us: 1.04x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 39.9 ms: 1.00x slower                                                  |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.25 sec: 1.01x slower                                                 |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                  |
| generators                       | 21.9 ms                                                  | 22.2 ms: 1.01x slower                                                  |
| sphinx                           | 434 ms                                                   | 439 ms: 1.01x slower                                                   |
| pycparser                        | 497 ms                                                   | 507 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                 |
| comprehensions                   | 9.84 us                                                  | 10.1 us: 1.03x slower                                                  |
| xml_etree_generate               | 38.9 ms                                                  | 40.8 ms: 1.05x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                  |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                  |
| go                               | 70.0 ms                                                  | 74.8 ms: 1.07x slower                                                  |
| thrift                           | 322 us                                                   | 346 us: 1.08x slower                                                   |
| pyflate                          | 216 ms                                                   | 234 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 59.4 ms: 1.09x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                   |
| spectral_norm                    | 54.4 ms                                                  | 59.3 ms: 1.09x slower                                                  |
| logging_silent                   | 50.9 ns                                                  | 55.7 ns: 1.09x slower                                                  |
| mdp                              | 1.09 sec                                                 | 1.20 sec: 1.10x slower                                                 |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.4 ms: 1.10x slower                                                  |
| raytrace                         | 145 ms                                                   | 159 ms: 1.10x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 63.7 ms: 1.11x slower                                                  |
| logging_simple                   | 2.57 us                                                  | 2.88 us: 1.12x slower                                                  |
| logging_format                   | 2.80 us                                                  | 3.15 us: 1.12x slower                                                  |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 9.08 ms: 1.13x slower                                                  |
| nqueens                          | 43.5 ms                                                  | 49.5 ms: 1.14x slower                                                  |
| 2to3                             | 114 ms                                                   | 130 ms: 1.14x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 81.0 us: 1.14x slower                                                  |
| xml_etree_process                | 26.7 ms                                                  | 30.5 ms: 1.14x slower                                                  |
| tomli_loads                      | 957 ms                                                   | 1.09 sec: 1.14x slower                                                 |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.92 ms: 1.14x slower                                                  |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.15x slower                                                   |
| chaos                            | 28.9 ms                                                  | 33.2 ms: 1.15x slower                                                  |
| python_startup                   | 8.01 ms                                                  | 9.21 ms: 1.15x slower                                                  |
| scimark_sor                      | 61.0 ms                                                  | 70.2 ms: 1.15x slower                                                  |
| sympy_str                        | 104 ms                                                   | 121 ms: 1.16x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 2.01 ms: 1.16x slower                                                  |
| connected_components             | 201 ms                                                   | 235 ms: 1.17x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.48 ms: 1.19x slower                                                  |
| crypto_pyaes                     | 38.8 ms                                                  | 46.5 ms: 1.20x slower                                                  |
| genshi_xml                       | 21.8 ms                                                  | 26.2 ms: 1.20x slower                                                  |
| async_tree_eager                 | 45.6 ms                                                  | 55.6 ms: 1.22x slower                                                  |
| json_dumps                       | 4.26 ms                                                  | 5.20 ms: 1.22x slower                                                  |
| sympy_expand                     | 167 ms                                                   | 204 ms: 1.22x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 171 us: 1.23x slower                                                   |
| richards                         | 22.4 ms                                                  | 27.6 ms: 1.23x slower                                                  |
| richards_super                   | 25.4 ms                                                  | 31.4 ms: 1.24x slower                                                  |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.25x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 13.1 ms: 1.25x slower                                                  |
| pprint_safe_repr                 | 328 ms                                                   | 412 ms: 1.26x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.6 ms: 1.26x slower                                                  |
| fannkuch                         | 176 ms                                                   | 223 ms: 1.27x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 844 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                  |
| meteor_contest                   | 47.7 ms                                                  | 60.9 ms: 1.27x slower                                                  |
| many_optionals                   | 195 us                                                   | 249 us: 1.28x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 66.7 ms: 1.30x slower                                                  |
| mako                             | 4.77 ms                                                  | 6.23 ms: 1.31x slower                                                  |
| hexiom                           | 3.04 ms                                                  | 3.99 ms: 1.31x slower                                                  |
| django_template                  | 13.6 ms                                                  | 18.2 ms: 1.33x slower                                                  |
| telco                            | 2.61 ms                                                  | 3.63 ms: 1.39x slower                                                  |
| nbody                            | 54.2 ms                                                  | 78.8 ms: 1.45x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 610 us: 1.46x slower                                                   |
| coverage                         | 26.9 ms                                                  | 40.7 ms: 1.51x slower                                                  |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                  |
| Geometric mean                   | (ref)                                                    | 1.02x slower                                                           |

Benchmark hidden because not significant (3): pylint, pidigits, regex_v8
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250324-3.14.0a6+-60f2173-NOGIL/bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x slower

# HPT report

- Reliability score: 99.44% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x