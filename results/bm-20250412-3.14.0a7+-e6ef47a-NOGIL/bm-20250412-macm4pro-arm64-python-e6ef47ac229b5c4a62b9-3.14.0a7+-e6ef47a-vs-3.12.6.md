# Results vs. 3.12.6

- fork: python
- ref: e6ef47ac229b5c4a62b9
- machine: darwin-arm64
- commit hash: e6ef47a
- commit date: 2025-04-12
- overall geometric mean: 1.114x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 984 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.2 ms: 2.02x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.39x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.04x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.3 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 53.6 ms: 1.01x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.89 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.7 ms: 1.40x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| tomli_loads          | 957 ms                                                   | 940 ms: 1.02x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.07x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.09x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.01 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.47 ms: 1.18x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.53 ms: 1.32x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| mako            | 4.77 ms                                                  | 5.40 ms: 1.13x slower                                                    |
| django_template | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 748 us: 2.68x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.71 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.2 ms: 2.02x faster                                                    |
| mdp                              | 1.09 sec                                                 | 557 ms: 1.96x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 446 us: 1.86x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.7 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.39x faster                                                     |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| deepcopy                         | 161 us                                                   | 121 us: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.27x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.5 us: 1.26x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 805 ns: 1.20x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.33 us: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                    |
| pylint                           | 128 ms                                                   | 110 ms: 1.17x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.6 ms: 1.16x faster                                                    |
| k_core                           | 1.12 sec                                                 | 978 ms: 1.14x faster                                                     |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.3 ms: 1.12x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.4 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 46.4 ns: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.60 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 984 ms: 1.04x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.49 us: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.1 ms: 1.03x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 940 ms: 1.02x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.89 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| nbody                            | 54.2 ms                                                  | 53.6 ms: 1.01x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.3 us: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.12 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 52.9 ms: 1.03x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.1 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.89 ms: 1.03x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.6 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                     |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.04x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.7 ms: 1.05x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.2 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 188 ms: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.07x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 354 ms: 1.08x slower                                                     |
| connected_components             | 201 ms                                                   | 217 ms: 1.08x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 725 ms: 1.09x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.09x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.64 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.40 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.8 ms: 1.15x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.01 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.47 ms: 1.18x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 239 us: 1.23x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.28 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.53 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 570 us: 1.36x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.1 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.3 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250412-3.14.0a7+-e6ef47a-NOGIL/bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.22x