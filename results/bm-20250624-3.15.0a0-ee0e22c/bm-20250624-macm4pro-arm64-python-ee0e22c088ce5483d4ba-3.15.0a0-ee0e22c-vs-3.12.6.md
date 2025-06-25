# Results vs. 3.12.6

- fork: python
- ref: ee0e22c088ce5483d4ba
- machine: darwin-arm64
- commit hash: ee0e22c
- commit date: 2025-06-24
- overall geometric mean: 1.098x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.1 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.3 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.2 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 926 ms: 1.03x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.75 ms: 2.13x faster                                                   |
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.41 us: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                   |
| float                            | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.7 ms: 1.21x faster                                                   |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.0 ms: 1.20x faster                                                   |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 947 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.0 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.3 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.8 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.2 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.48 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.0 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.7 ms: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 926 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 137 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.6 ms: 1.02x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 25.1 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.01x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 99.1 ms: 1.01x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.60 us: 1.01x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| pycparser                        | 497 ms                                                   | 504 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.5 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| pprint_pformat                   | 665 ms                                                   | 686 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 339 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.4 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 947 us: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 199 ns: 3.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (5): logging_format, shortest_path, json, 2to3, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x