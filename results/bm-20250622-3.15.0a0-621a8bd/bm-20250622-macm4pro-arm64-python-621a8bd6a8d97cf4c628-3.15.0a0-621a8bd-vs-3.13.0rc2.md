# Results vs. 3.13.0rc2

- fork: python
- ref: 621a8bd6a8d97cf4c628
- machine: darwin-arm64
- commit hash: 621a8bd
- commit date: 2025-06-22
- overall geometric mean: 1.022x faster
- HPT reliability: 69.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.49x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.8 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 934 ms: 1.07x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.48 ms: 1.04x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.6 ms: 1.00x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 64.5 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 4.87 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 516 ms: 2.05x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 949 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                   |
| go                               | 72.6 ms                                                        | 56.5 ms: 1.28x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 934 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.48 ms: 1.04x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 959 us: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.9 us: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.6 ms: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.8 ms: 1.00x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 968 ns: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 64.5 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 499 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.9 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.39 us: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.87 ms: 1.10x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 719 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.76 us: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.2 ms: 1.15x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.77 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.8 ms: 3.07x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 198 ns: 4.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (5): xml_etree_process, sympy_integrate, spectral_norm, richards, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250622-3.15.0a0-621a8bd/bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 69.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x