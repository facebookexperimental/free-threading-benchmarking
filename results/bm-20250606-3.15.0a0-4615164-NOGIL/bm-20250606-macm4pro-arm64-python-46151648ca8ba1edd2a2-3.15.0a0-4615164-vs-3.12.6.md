# Results vs. 3.12.6

- fork: python
- ref: 46151648ca8ba1edd2a2
- machine: darwin-arm64
- commit hash: 4615164
- commit date: 2025-06-06
- overall geometric mean: 1.106x faster
- HPT reliability: 99.54%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 982 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 189 ms: 2.36x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.7 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.88x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.4 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 232 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.5 ms: 1.06x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.5 ms: 2.38x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.40x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.06 ms: 1.06x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 978 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.39 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.84 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                   |
| mako            | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 764 us: 2.63x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 189 ms: 2.36x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.57 ms: 2.17x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 85.7 ms: 2.01x faster                                                   |
| mdp                              | 1.09 sec                                                 | 555 ms: 1.97x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.88x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.4 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 481 us: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 232 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.75 us: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| go                               | 70.0 ms                                                  | 60.7 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 130 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.4 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.8 ms: 1.07x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.06 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 982 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.88 ms: 1.02x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 3.00 ms: 1.01x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| chaos                            | 28.9 ms                                                  | 29.2 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| thrift                           | 322 us                                                   | 327 us: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 978 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.8 us: 1.03x slower                                                   |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.5 ms: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.4 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 41.2 ms: 1.06x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.5 ms: 1.06x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.78 us: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.06 us: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.5 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.0 ms: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 372 ms: 1.14x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 759 ms: 1.14x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.39 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.84 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.27 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 66.5 ms: 1.30x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 594 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.8 ms: 1.48x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.5 ms: 2.38x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 214 ns: 4.21x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): html5lib, nbody
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250606-3.15.0a0-4615164-NOGIL/bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.106x faster

# HPT report

- Reliability score: 99.54% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x