# Results vs. 3.12.6

- fork: python
- ref: 52be7f445e454ccb44e3
- machine: darwin-arm64
- commit hash: 52be7f4
- commit date: 2025-06-18
- overall geometric mean: 1.089x faster
- HPT reliability: 95.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 424 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.95 ms: 1.36x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.2 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| nbody          | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.49 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.7 ms: 1.03x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.97 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.74 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 787 us: 2.55x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.76 ms: 2.13x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 567 ms: 1.93x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 490 us: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.95 ms: 1.36x faster                                                   |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| deepcopy                         | 161 us                                                   | 121 us: 1.33x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.32x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.84 us: 1.25x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 827 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 61.0 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 130 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.9 ms: 1.11x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 49.4 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.9 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 424 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.49 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.99 ms: 1.00x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 3.03 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.1 us: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 329 us: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.7 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.4 ms: 1.09x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.10x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.9 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 222 ms: 1.10x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.85 us: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.15 us: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.8 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.0 ms: 1.13x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 376 ms: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 767 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.74 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.97 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.19 ms: 1.22x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 69.5 ms: 1.35x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 593 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.2 ms: 2.43x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 219 ns: 4.31x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 95.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x