# Results vs. 3.13.0rc2

- fork: python
- ref: 49e83e31bd45e513a3ca
- machine: darwin-arm64
- commit hash: 49e83e3
- commit date: 2025-09-22
- overall geometric mean: 1.021x faster
- HPT reliability: 58.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 969 ms: 1.08x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.7 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 238 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.0 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 94.2 ms: 1.00x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 52.0 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.7 ms: 1.26x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 947 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.89 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| django_template | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| mako            | 4.41 ms                                                        | 5.74 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 746 us: 2.74x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 468 us: 2.12x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| mdp                              | 1.06 sec                                                       | 592 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.7 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.27x faster                                                   |
| deepcopy                         | 145 us                                                         | 115 us: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.7 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 238 ms: 1.23x faster                                                    |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.20x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 828 ns: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| docutils                         | 1.05 sec                                                       | 969 ms: 1.08x faster                                                    |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                   |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 947 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.97 ms: 1.03x faster                                                   |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 94.2 ms: 1.00x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.89 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.0 ms: 1.08x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.3 ns: 1.09x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 711 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.12x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 59.7 ms: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.16x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.89 ms: 1.16x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.9 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.27 us: 1.21x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.5 ms: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.29 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.74 ms: 1.30x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.1 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.0 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 591 us: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 332 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250922-3.15.0a0-49e83e3-NOGIL/bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 58.67% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.21x