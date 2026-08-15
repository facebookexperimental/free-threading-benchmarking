# Results vs. 3.12.6

- fork: python
- ref: dffac6163e693cf80ed4
- machine: darwin-arm64
- commit hash: dffac61
- commit date: 2026-08-14
- overall geometric mean: 1.126x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 967 ms: 1.06x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.8 ms: 1.06x faster                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 314 ms: 1.58x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 123 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 335 ms: 1.43x faster                                                    |
| async_generators                 | 206 ms                                                   | 146 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 128 ms: 1.35x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 339 ms: 1.32x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 180 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 296 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 267 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| nbody          | 54.2 ms                                                  | 41.9 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 170 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 55.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| tomli_loads          | 957 ms                                                   | 852 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 68.4 ms: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.42 ms: 1.13x slower                                                   |
| python_startup         | 8.01 ms                                                  | 9.27 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.20 ms: 4.95x faster                                                   |
| pylint                           | 128 ms                                                   | 57.5 ms: 2.23x faster                                                   |
| mdp                              | 1.09 sec                                                 | 528 ms: 2.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 314 ms: 1.58x faster                                                    |
| deepcopy                         | 161 us                                                   | 102 us: 1.58x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.76 us: 1.46x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 123 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 335 ms: 1.43x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 49.7 us: 1.43x faster                                                   |
| async_generators                 | 206 ms                                                   | 146 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 128 ms: 1.35x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 339 ms: 1.32x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| go                               | 70.0 ms                                                  | 54.1 ms: 1.30x faster                                                   |
| nbody                            | 54.2 ms                                                  | 41.9 ms: 1.30x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.2 ms: 1.29x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 48.8 ms: 1.25x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 180 ms: 1.24x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.23x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.6 ms: 1.22x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.23 us: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.0 ms: 1.15x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 296 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.82 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 852 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.12x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.7 ms: 1.08x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.6 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                   |
| fannkuch                         | 176 ms                                                   | 164 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.57 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 967 ms: 1.06x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.8 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 927 ns: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 318 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.1 ms: 1.03x faster                                                   |
| thrift                           | 322 us                                                   | 314 us: 1.03x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 655 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 68.4 ms: 1.01x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 426 us: 1.02x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 55.5 ms: 1.02x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 847 us: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.02x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| connected_components             | 201 ms                                                   | 210 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 170 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.42 ms: 1.13x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.27 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 267 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (5): json, scimark_lu, json_loads, asyncio_websockets, pycparser
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260814-3.16.0a0-dffac61/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.126x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x