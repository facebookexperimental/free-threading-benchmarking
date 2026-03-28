# Results vs. 3.12.6

- fork: python
- ref: a933e9ccee6d3c6753db
- machine: darwin-arm64
- commit hash: a933e9c
- commit date: 2026-03-28
- overall geometric mean: 1.117x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 967 ms: 1.06x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.05x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.3 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.1 ms: 2.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.05 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                    |
| tomli_loads          | 957 ms                                                   | 850 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.02x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.99 ms: 5.20x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 769 us: 2.61x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| mdp                              | 1.09 sec                                                 | 597 ms: 1.83x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 490 us: 1.69x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.48x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 789 ns: 1.22x faster                                                     |
| go                               | 70.0 ms                                                  | 58.7 ms: 1.19x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.26 us: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.2 ns: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| raytrace                         | 145 ms                                                   | 125 ms: 1.16x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.1 ms: 1.13x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 850 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.32 us: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 450 ms: 1.11x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.55 us: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.7 ms: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.8 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.6 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.05 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 967 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.05x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.95 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 662 ms: 1.00x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.1 us: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.3 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.02x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 52.4 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.8 ms: 1.04x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| thrift                           | 322 us                                                   | 336 us: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| nbody                            | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.3 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.96 ms: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.1 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.4 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.14x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 256 us: 1.31x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.0 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.1 ms: 2.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (2): json, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260328-3.15.0a7+-a933e9c-NOGIL/bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.117x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.39x