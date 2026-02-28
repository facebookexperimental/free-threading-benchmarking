# Results vs. 3.12.6

- fork: python
- ref: 180d58cbcc0f7f34d6ba
- machine: darwin-arm64
- commit hash: 180d58c
- commit date: 2026-02-28
- overall geometric mean: 1.090x faster
- HPT reliability: 99.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                     |
| sphinx         | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.4 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.6 ms: 2.94x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                    |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| tomli_loads          | 957 ms                                                   | 862 ms: 1.11x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.2 ms: 1.27x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.38 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.17 ms: 4.98x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 819 us: 2.45x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 605 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 516 us: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 792 ns: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.30 us: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.4 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.7 ns: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 862 ms: 1.11x faster                                                     |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.41 us: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.06x faster                                                     |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                     |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.6 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 327 ms: 1.00x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 668 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.09 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.4 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.4 us: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.21 ms: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.8 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.1 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 59.9 ms: 1.17x slower                                                    |
| shortest_path                    | 219 ms                                                   | 256 ms: 1.17x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.9 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.2 ms: 1.27x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.38 ms: 1.29x slower                                                    |
| many_optionals                   | 195 us                                                   | 271 us: 1.39x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 585 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.6 ms: 2.94x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (3): docutils, html5lib, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260228-3.15.0a6+-180d58c-NOGIL/bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 99.46% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.38x