# Results vs. 3.12.6

- fork: python
- ref: ed672f7a8a3c843d8e6e
- machine: darwin-arm64
- commit hash: ed672f7
- commit date: 2025-10-19
- overall geometric mean: 1.083x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.7 ms: 1.08x slower                                                    |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                                    |
| nbody          | 54.2 ms                                                  | 51.2 ms: 1.06x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (2): json_loads, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.36 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| mako            | 4.77 ms                                                  | 5.01 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 548 ms: 1.99x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.48x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.57 us: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.2 ns: 1.21x faster                                                    |
| float                            | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 58.2 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                    |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 53.3 ms: 1.15x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.2 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.9 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 66.0 us: 1.07x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.49 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                    |
| nbody                            | 54.2 ms                                                  | 51.2 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.91 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.1 ms: 1.04x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.7 ms: 1.03x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.9 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 57.0 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 677 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 336 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.9 ms: 1.05x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.01 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.4 ms: 1.07x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.7 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                     |
| fannkuch                         | 176 ms                                                   | 190 ms: 1.08x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 921 us: 1.11x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.36 ms: 1.11x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 375 us: 1.92x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (6): bench_thread_pool, thrift, sqlite_synth, json_loads, pycparser, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251019-3.15.0a1+-ed672f7/bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x