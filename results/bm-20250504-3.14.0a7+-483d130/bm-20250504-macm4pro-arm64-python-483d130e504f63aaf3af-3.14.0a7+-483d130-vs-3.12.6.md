# Results vs. 3.12.6

- fork: python
- ref: 483d130e504f63aaf3af
- machine: darwin-arm64
- commit hash: 483d130
- commit date: 2025-05-04
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 108 ms: 1.05x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 25.6 ms: 1.11x slower                                                    |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 244 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.68x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                    |
| nbody          | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.99 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.9 us: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 945 ms: 1.01x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.00 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.05 ms: 1.06x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.16 ms: 2.27x faster                                                    |
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 244 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.68x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.31x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.59 us: 1.30x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.0 ms: 1.29x faster                                                    |
| float                            | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.1 ns: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| go                               | 70.0 ms                                                  | 56.1 ms: 1.25x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.4 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 51.2 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 47.1 ms: 1.15x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| nbody                            | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.33 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.2 us: 1.09x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.5 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.3 ms: 1.06x faster                                                    |
| 2to3                             | 114 ms                                                   | 108 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.97 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.9 us: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.0 ms: 1.04x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.7 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 938 ns: 1.03x faster                                                     |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 649 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 945 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 324 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| connected_components             | 201 ms                                                   | 200 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                     |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 435 us: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.99 ms: 1.04x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.40 ms: 1.04x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 869 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.05 ms: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 25.6 ms: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.00 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (4): gc_traversal, json, bench_mp_pool, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250504-3.14.0a7+-483d130/bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x