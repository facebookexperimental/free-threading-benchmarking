# Results vs. 3.12.6

- fork: python
- ref: 6d5a8c2ec19f1c38b455
- machine: darwin-arm64
- commit hash: 6d5a8c2
- commit date: 2025-05-09
- overall geometric mean: 1.106x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| html5lib       | 23.0 ms                                                  | 25.9 ms: 1.13x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.2 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                   |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.89 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.5 us: 1.03x faster                                                   |
| tomli_loads          | 957 ms                                                   | 930 ms: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 5.14 ms: 1.21x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.45 ms: 1.05x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.05 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| mako            | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.32 ms: 2.23x faster                                                   |
| mdp                              | 1.09 sec                                                 | 529 ms: 2.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.47x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.72 us: 1.28x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.26x faster                                                   |
| go                               | 70.0 ms                                                  | 56.4 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.6 ms: 1.18x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| spectral_norm                    | 54.4 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.0 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.09x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 302 us: 1.07x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 66.6 us: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.2 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.96 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.4 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 99.5 us: 1.03x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.9 ms: 1.03x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 930 ms: 1.03x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.7 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 651 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 321 ms: 1.02x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 951 ns: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.58 us: 1.01x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| regex_v8                         | 9.59 ms                                                  | 9.89 ms: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.45 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.05 ms: 1.06x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.9 ms: 1.08x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 913 us: 1.10x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 25.9 ms: 1.13x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.17x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 5.14 ms: 1.21x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 240 us: 1.23x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.2 ms: 2.68x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 194 ns: 3.82x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (4): regex_dna, connected_components, logging_format, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-6d5a8c2/bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.106x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x