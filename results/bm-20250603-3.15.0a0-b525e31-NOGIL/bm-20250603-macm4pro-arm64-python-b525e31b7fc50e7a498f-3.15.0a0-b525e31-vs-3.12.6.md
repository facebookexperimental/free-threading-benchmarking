# Results vs. 3.12.6

- fork: python
- ref: b525e31b7fc50e7a498f
- machine: darwin-arm64
- commit hash: b525e31
- commit date: 2025-06-03
- overall geometric mean: 1.100x faster
- HPT reliability: 99.17%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 995 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.9 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                   |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.9 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 972 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.68 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.42 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                   |
| mako            | 4.77 ms                                                  | 5.75 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.61x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.75 ms: 2.13x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 557 ms: 1.96x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 480 us: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                   |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.87 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.17x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 829 ns: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 60.7 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 130 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.7 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.9 ms: 1.04x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 995 ms: 1.03x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.98 ms: 1.02x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.88 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 972 ms: 1.02x slower                                                    |
| thrift                           | 322 us                                                   | 330 us: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.9 us: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.4 ms: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 59.7 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.9 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.81 us: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.68 ms: 1.10x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 52.7 ms: 1.10x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.10 us: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.4 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 376 ms: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 768 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.42 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.75 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.26 ms: 1.25x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 66.1 ms: 1.29x slower                                                   |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 595 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): pidigits, nbody
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 99.17% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x