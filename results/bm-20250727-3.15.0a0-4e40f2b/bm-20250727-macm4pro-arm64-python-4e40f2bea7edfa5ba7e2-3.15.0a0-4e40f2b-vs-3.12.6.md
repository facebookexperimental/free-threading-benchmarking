# Results vs. 3.12.6

- fork: python
- ref: 4e40f2bea7edfa5ba7e2
- machine: darwin-arm64
- commit hash: 4e40f2b
- commit date: 2025-07-27
- overall geometric mean: 1.098x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.2 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.3 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.6 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.4 us: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 931 ms: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 536 ms: 2.04x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.49 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.4 ns: 1.26x faster                                                   |
| float                            | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.6 ms: 1.25x faster                                                   |
| go                               | 70.0 ms                                                  | 56.1 ms: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.0 ms: 1.20x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                   |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 954 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.3 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 63.7 us: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.3 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.6 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.46 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.0 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.8 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.6 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 99.4 us: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 931 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.2 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.3 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 653 ms: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 960 ns: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 435 us: 1.04x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.05x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.9 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 943 us: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 323 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): pycparser, regex_v8, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x