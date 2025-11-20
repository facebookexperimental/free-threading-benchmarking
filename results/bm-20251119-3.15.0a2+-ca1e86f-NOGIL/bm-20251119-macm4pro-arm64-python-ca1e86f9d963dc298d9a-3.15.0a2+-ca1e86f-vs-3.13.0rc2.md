# Results vs. 3.13.0rc2

- fork: python
- ref: ca1e86f9d963dc298d9a
- machine: darwin-arm64
- commit hash: ca1e86f
- commit date: 2025-11-19
- overall geometric mean: 1.033x faster
- HPT reliability: 53.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 194 ms: 2.09x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.89x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 83.3 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 121 ms: 1.53x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 96.7 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 127 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.9 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.9 ms: 2.62x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.4 ms: 1.19x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| nbody          | 42.5 ms                                                        | 53.7 ms: 1.26x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 864 ms: 1.16x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.04x slower                                                     |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.91 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.19 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.8 ms: 1.09x slower                                                    |
| mako            | 4.41 ms                                                        | 5.49 ms: 1.24x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 776 us: 2.63x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 194 ms: 2.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 481 us: 2.06x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.89x faster                                                     |
| mdp                              | 1.06 sec                                                       | 601 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 83.3 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 121 ms: 1.53x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 96.7 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 127 ms: 1.46x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.39x faster                                                    |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| go                               | 72.6 ms                                                        | 57.0 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                     |
| float                            | 31.4 ms                                                        | 26.4 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.8 ms: 1.17x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 819 ns: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 864 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| docutils                         | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.97 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 459 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.02x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.5 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 673 ms: 1.04x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.04x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.98 ms: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.9 ms: 1.05x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.8 ns: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.9 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.01 ms: 1.06x slower                                                    |
| dask                             | 525 ms                                                         | 560 ms: 1.07x slower                                                     |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.07x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.08x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.8 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.6 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 48.2 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.5 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| raytrace                         | 109 ms                                                         | 123 ms: 1.13x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 73.6 us: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.91 ms: 1.15x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 184 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.4 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.03 us: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.19 ms: 1.21x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.9 ms: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.2 ms: 1.22x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.49 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.4 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                    |
| nbody                            | 42.5 ms                                                        | 53.7 ms: 1.26x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 547 us: 1.33x slower                                                     |
| many_optionals                   | 200 us                                                         | 374 us: 1.86x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.9 ms: 2.62x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.7 ms: 2.99x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251119-3.15.0a2+-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 53.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x