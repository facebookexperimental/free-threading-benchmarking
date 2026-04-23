# Results vs. 3.12.6

- fork: python
- ref: 79321fdce3227cf09bb8
- machine: darwin-arm64
- commit hash: 79321fd
- commit date: 2026-04-22
- overall geometric mean: 1.177x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.6 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.2 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.4 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.8 ms: 1.29x faster                                                    |
| tomli_loads          | 957 ms                                                   | 809 ms: 1.18x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.6 us: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.2 ms: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.84 ms: 1.02x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.83 ms: 1.07x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.68 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.95 ms: 5.26x faster                                                    |
| pylint                           | 128 ms                                                   | 50.4 ms: 2.54x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.05x faster                                                     |
| mdp                              | 1.09 sec                                                 | 533 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.6 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.3 us: 1.66x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.01 us: 1.40x faster                                                    |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                    |
| go                               | 70.0 ms                                                  | 51.9 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.8 ms: 1.29x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.5 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 896 ms: 1.25x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 35.2 ms: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.1 ns: 1.21x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.6 ms: 1.21x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 809 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.2 ms: 1.14x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.7 us: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 95.6 us: 1.08x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.9 ms: 1.07x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.83 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 629 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.4 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.2 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 938 ns: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.68 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 425 us: 1.02x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 5.84 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 939 us: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.42 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.2 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (5): regex_v8, pidigits, 2to3, crypto_pyaes, pickle_pure_python
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260422-3.15.0a8+-79321fd/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.177x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.24x