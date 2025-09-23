# Results vs. 3.12.6

- fork: python
- ref: 49e83e31bd45e513a3ca
- machine: darwin-arm64
- commit hash: 49e83e3
- commit date: 2025-09-22
- overall geometric mean: 1.125x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 246 ms: 1.95x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.87 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.0 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.0 ms: 2.64x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.7 ms: 1.21x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.75 ms: 1.13x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| tomli_loads          | 957 ms                                                   | 892 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.0 us: 1.05x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.84 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 524 ms: 2.08x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 246 ms: 1.95x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.52x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.87 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.32x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.44 us: 1.32x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.1 ms: 1.29x faster                                                   |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.1 ms: 1.26x faster                                                   |
| go                               | 70.0 ms                                                  | 55.6 ms: 1.26x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.24x faster                                                   |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.7 ms: 1.21x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.3 ms: 1.20x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.3 ms: 1.20x faster                                                   |
| k_core                           | 1.12 sec                                                 | 951 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                   |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.16x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.14x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.75 ms: 1.13x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.27 us: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.0 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.26 ms: 1.10x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                   |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 46.8 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 892 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.84 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.1 ms: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.3 ms: 1.06x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 54.7 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.0 us: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 937 ns: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 331 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.01x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 40.9 ms: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 901 us: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.5 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 312 us: 1.60x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.0 ms: 2.64x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (6): pprint_pformat, gc_traversal, fannkuch, regex_v8, sympy_expand, connected_components
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250922-3.15.0a0-49e83e3/bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.125x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.15x