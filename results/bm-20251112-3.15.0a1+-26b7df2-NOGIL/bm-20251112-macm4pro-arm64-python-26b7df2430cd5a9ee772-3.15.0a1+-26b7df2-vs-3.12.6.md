# Results vs. 3.12.6

- fork: python
- ref: 26b7df2430cd5a9ee772
- machine: darwin-arm64
- commit hash: 26b7df2
- commit date: 2025-11-12
- overall geometric mean: 1.084x faster
- HPT reliability: 98.21%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 87.9 ms: 1.96x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 55.6 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.8 ms: 1.04x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.48 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.1 ms: 1.17x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.06 ms: 1.05x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.04x faster                                                    |
| tomli_loads          | 957 ms                                                   | 937 ms: 1.02x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 27.4 ms: 1.02x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.80 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.11 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| mako            | 4.77 ms                                                  | 5.61 ms: 1.18x slower                                                    |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 769 us: 2.61x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 87.9 ms: 1.96x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                     |
| mdp                              | 1.09 sec                                                 | 609 ms: 1.79x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 483 us: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| deepcopy                         | 161 us                                                   | 115 us: 1.40x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.1 ms: 1.17x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.47 us: 1.16x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 836 ns: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| go                               | 70.0 ms                                                  | 60.8 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.8 ns: 1.14x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.5 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| raytrace                         | 145 ms                                                   | 131 ms: 1.10x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.9 ms: 1.09x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 19.2 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.06 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.8 ms: 1.04x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 937 ms: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.48 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.78 us: 1.01x faster                                                    |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.00x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.00x slower                                                    |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                     |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 44.4 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.4 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.6 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.2 us: 1.05x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 342 us: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 719 ms: 1.08x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.26 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                    |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.61 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 57.2 ms: 1.20x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.80 ms: 1.22x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.11 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.31x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 68.0 ms: 1.33x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.4 ms: 1.50x slower                                                    |
| many_optionals                   | 195 us                                                   | 390 us: 2.00x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_eager_memoization_tg
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251112-3.15.0a1+-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 98.21% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x