# Results vs. 3.12.6

- fork: python
- ref: c461aa99e2fabbaf5859
- machine: darwin-arm64
- commit hash: c461aa9
- commit date: 2026-01-15
- overall geometric mean: 1.156x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.2 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.7 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 171 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.5 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.7 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.86 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| tomli_loads          | 957 ms                                                   | 854 ms: 1.12x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 96.2 us: 1.07x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.61 ms: 1.16x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.76 ms: 1.07x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.06 ms: 5.12x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.5 us: 1.64x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.04 us: 1.40x faster                                                    |
| float                            | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 52.9 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.5 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                    |
| k_core                           | 1.12 sec                                                 | 910 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.5 ms: 1.20x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| nbody                            | 54.2 ms                                                  | 45.7 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.5 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.0 ms: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.43 us: 1.15x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.8 us: 1.15x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.0 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 854 ms: 1.12x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.76 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 621 ms: 1.07x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 96.2 us: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.7 ms: 1.02x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.86 ms: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 208 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 171 ms: 1.06x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.9 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 955 us: 1.15x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.61 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.2 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.7 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 257 us: 1.32x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.2 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (2): sqlite_synth, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260115-3.15.0a5+-c461aa9/bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.156x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x