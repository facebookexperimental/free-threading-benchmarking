# Results vs. 3.12.6

- fork: python
- ref: 86513f6c2ebdd1fb692c
- machine: darwin-arm64
- commit hash: 86513f6
- commit date: 2025-11-10
- overall geometric mean: 1.069x faster
- HPT reliability: 92.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.11x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.39x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 203 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 199 ms: 2.24x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 214 ms: 2.15x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 89.8 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 113 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.3 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.1 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.8 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.40 ms: 1.02x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.13 ms: 1.03x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| tomli_loads          | 957 ms                                                   | 984 ms: 1.03x slower                                                     |
| xml_etree_process    | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.79 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.9 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.94 ms: 1.24x slower                                                    |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 767 us: 2.62x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.39x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 203 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 199 ms: 2.24x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 214 ms: 2.15x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 89.8 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 616 ms: 1.77x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 476 us: 1.74x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.4 us: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                    |
| float                            | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.58 us: 1.15x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 853 ns: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| go                               | 70.0 ms                                                  | 62.9 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.10x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 46.2 ns: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.9 ms: 1.09x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| raytrace                         | 145 ms                                                   | 135 ms: 1.08x faster                                                     |
| pyflate                          | 216 ms                                                   | 202 ms: 1.07x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 19.5 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 52.0 ms: 1.05x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 136 ms: 1.04x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.13 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 482 ms: 1.03x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.40 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 113 ms: 1.01x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.59 us: 1.01x slower                                                    |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.13 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| chaos                            | 28.9 ms                                                  | 29.7 ms: 1.03x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 984 ms: 1.03x slower                                                     |
| nqueens                          | 43.5 ms                                                  | 44.8 ms: 1.03x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 75.3 us: 1.06x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.8 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 188 ms: 1.07x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.5 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.7 ms: 1.07x slower                                                    |
| thrift                           | 322 us                                                   | 346 us: 1.07x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.25 ms: 1.08x slower                                                    |
| sympy_str                        | 104 ms                                                   | 114 ms: 1.09x slower                                                     |
| richards                         | 22.4 ms                                                  | 24.5 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.9 ms: 1.10x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.3 ms: 1.10x slower                                                    |
| 2to3                             | 114 ms                                                   | 126 ms: 1.11x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.6 ms: 1.12x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 368 ms: 1.12x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 747 ms: 1.12x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.1 ms: 1.13x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.9 ms: 1.14x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 195 ms: 1.17x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 57.0 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.79 ms: 1.22x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.94 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 533 us: 1.27x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                    |
| many_optionals                   | 195 us                                                   | 389 us: 1.99x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.1 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                             |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251110-3.15.0a1+-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 92.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x