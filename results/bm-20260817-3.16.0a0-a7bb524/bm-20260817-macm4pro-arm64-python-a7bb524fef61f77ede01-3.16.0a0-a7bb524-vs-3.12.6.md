# Results vs. 3.12.6

- fork: python
- ref: a7bb524fef61f77ede01
- machine: darwin-arm64
- commit hash: a7bb524
- commit date: 2026-08-17
- overall geometric mean: 1.127x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 964 ms: 1.06x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 317 ms: 1.56x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 334 ms: 1.44x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 124 ms: 1.43x faster                                                    |
| async_generators                 | 206 ms                                                   | 147 ms: 1.40x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 128 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 346 ms: 1.29x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 181 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 288 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 267 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 42.1 ms: 1.29x faster                                                   |
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.16x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 55.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.61 ms: 1.18x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| tomli_loads          | 957 ms                                                   | 851 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.5 us: 1.03x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.0 ms: 1.03x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 68.7 ms: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                   |
| python_startup         | 8.01 ms                                                  | 9.11 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                   |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.18 ms: 4.97x faster                                                   |
| pylint                           | 128 ms                                                   | 57.3 ms: 2.24x faster                                                   |
| mdp                              | 1.09 sec                                                 | 526 ms: 2.08x faster                                                    |
| deepcopy                         | 161 us                                                   | 100 us: 1.61x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 317 ms: 1.56x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.80 us: 1.45x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 334 ms: 1.44x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 124 ms: 1.43x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 50.3 us: 1.41x faster                                                   |
| async_generators                 | 206 ms                                                   | 147 ms: 1.40x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 128 ms: 1.34x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                   |
| go                               | 70.0 ms                                                  | 53.3 ms: 1.31x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 346 ms: 1.29x faster                                                    |
| nbody                            | 54.2 ms                                                  | 42.1 ms: 1.29x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.3 ms: 1.29x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 181 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.5 ms: 1.22x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.5 ns: 1.20x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.61 ms: 1.18x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 288 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.81 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.4 ms: 1.14x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 851 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.7 ms: 1.08x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| fannkuch                         | 176 ms                                                   | 165 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 964 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.62 ms: 1.05x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 922 ns: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.5 us: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.95 ms: 1.03x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.0 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.3 ms: 1.02x faster                                                   |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 651 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 51.0 ms: 1.01x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 835 us: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 68.7 ms: 1.01x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 425 us: 1.01x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 55.5 ms: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                   |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.11 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 267 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (3): async_tree_eager_cpu_io_mixed, pycparser, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.127x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x