# Results vs. 3.12.6

- fork: python
- ref: 4e7e2dd043c1da85b0c1
- machine: darwin-arm64
- commit hash: 4e7e2dd
- commit date: 2025-10-02
- overall geometric mean: 1.083x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.88x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.7 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.9 ms: 1.19x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.6 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.95 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.9 ms: 1.20x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.7 ms: 1.10x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (2): json_loads, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.69 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.4 ms: 1.01x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                   |
| mako            | 4.77 ms                                                  | 5.13 ms: 1.08x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 552 ms: 1.98x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.88x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                   |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.76 us: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                   |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.9 ms: 1.20x faster                                                   |
| go                               | 70.0 ms                                                  | 58.8 ms: 1.19x faster                                                   |
| float                            | 37.9 ms                                                  | 31.9 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                   |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.0 ns: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.3 ms: 1.14x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.2 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.11x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.7 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 65.1 us: 1.09x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.0 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.08x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.6 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.41 us: 1.07x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.7 ms: 1.07x faster                                                   |
| pyflate                          | 216 ms                                                   | 204 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.0 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.94 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.3 ms: 1.02x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.2 ms: 1.02x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 25.0 ms: 1.01x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.4 ms: 1.01x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.01x faster                                                   |
| thrift                           | 322 us                                                   | 320 us: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                    |
| pycparser                        | 497 ms                                                   | 505 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| pprint_pformat                   | 665 ms                                                   | 682 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 339 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.95 ms: 1.04x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.13 ms: 1.08x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 51.4 ms: 1.08x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.69 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| fannkuch                         | 176 ms                                                   | 192 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 919 us: 1.11x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 330 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (4): sqlite_synth, json, json_loads, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x