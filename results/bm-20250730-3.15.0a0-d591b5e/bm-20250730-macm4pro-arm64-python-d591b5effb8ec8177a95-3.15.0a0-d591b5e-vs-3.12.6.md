# Results vs. 3.12.6

- fork: python
- ref: d591b5effb8ec8177a95
- machine: darwin-arm64
- commit hash: d591b5e
- commit date: 2025-07-30
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.3 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.3 ms: 1.25x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 925 ms: 1.04x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.86 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 540 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.50 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| go                               | 70.0 ms                                                  | 55.7 ms: 1.26x faster                                                   |
| float                            | 37.9 ms                                                  | 30.3 ms: 1.25x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.3 ms: 1.23x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.3 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 956 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 63.4 us: 1.12x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.78 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.56 us: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.6 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.8 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 302 us: 1.06x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.1 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 49.2 ms: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.9 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 925 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 654 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 956 ns: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 324 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                   |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.86 ms: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| json_dumps                       | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.8 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.9 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 940 us: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 320 us: 1.64x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.3 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): pycparser, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x