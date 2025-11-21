# Results vs. 3.13.0rc2

- fork: python
- ref: 77cb39e0c7ef606ef68a
- machine: darwin-arm64
- commit hash: 77cb39e
- commit date: 2025-11-20
- overall geometric mean: 1.020x faster
- HPT reliability: 53.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.73x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 200 ms: 2.63x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.3 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.7 ms: 1.44x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.8 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 54.9 ms: 1.29x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.36 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 57.2 ms: 1.09x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.75 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.08 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| mako            | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.73x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 765 us: 2.67x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 200 ms: 2.63x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 475 us: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| mdp                              | 1.06 sec                                                       | 595 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.3 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.7 ms: 1.44x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| go                               | 72.6 ms                                                        | 58.8 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                     |
| float                            | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.36 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.2 ms: 1.09x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 334 ms: 1.04x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 685 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.1 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| dask                             | 525 ms                                                         | 561 ms: 1.07x slower                                                     |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 332 us: 1.07x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.4 ns: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.7 us: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.75 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.2 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.06 us: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.08 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.3 ms: 1.23x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                    |
| nbody                            | 42.5 ms                                                        | 54.9 ms: 1.29x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 561 us: 1.36x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 64.4 ms: 1.51x slower                                                    |
| many_optionals                   | 200 us                                                         | 376 us: 1.88x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.8 ms: 2.65x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.6 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251120-3.15.0a2+-77cb39e-NOGIL/bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 53.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x