# Results vs. 3.13.0rc2

- fork: python
- ref: 3cfab449ab1e3c1472d2
- machine: darwin-arm64
- commit hash: 3cfab44
- commit date: 2025-04-21
- overall geometric mean: 1.031x faster
- HPT reliability: 57.36%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 977 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.0 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.07x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.4 ms: 1.17x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.8 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 53.3 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| regex_compile  | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 35.6 ms: 1.30x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 929 ms: 1.08x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.3 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.05 ms: 1.09x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.1 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.49 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.54 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| mako            | 4.41 ms                                                        | 5.39 ms: 1.22x slower                                                    |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 747 us: 2.73x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 442 us: 2.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.07x faster                                                     |
| mdp                              | 1.06 sec                                                       | 556 ms: 1.90x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.0 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| k_core                           | 1.46 sec                                                       | 981 ms: 1.49x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 35.6 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 60.4 ms: 1.20x faster                                                    |
| deepcopy                         | 145 us                                                         | 121 us: 1.19x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 806 ns: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.6 ms: 1.17x faster                                                    |
| float                            | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 929 ms: 1.08x faster                                                     |
| docutils                         | 1.05 sec                                                       | 977 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 458 ms: 1.03x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.3 ms: 1.02x slower                                                    |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.04x slower                                                    |
| connected_components             | 208 ms                                                         | 217 ms: 1.04x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.87 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.5 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.07x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.06 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.05 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.49 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 355 ms: 1.10x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.40 ms: 1.11x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.2 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 48.8 ms: 1.12x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.2 us: 1.12x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.1 us: 1.12x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 731 ms: 1.13x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.66 ms: 1.13x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 46.4 ns: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.2 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.3 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.1 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.4 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                     |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 12.8 ms: 1.19x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.4 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.30 us: 1.22x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.39 ms: 1.22x slower                                                    |
| nbody                            | 42.5 ms                                                        | 53.3 ms: 1.25x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.4 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.54 ms: 1.27x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.6 ms: 1.28x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.59 ms: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 574 us: 1.39x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250421-3.14.0a7+-3cfab44-NOGIL/bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 57.36% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.17x