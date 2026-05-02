# Results vs. 3.13.0rc2

- fork: python
- ref: be9c7cb4b50f8007b610
- machine: darwin-arm64
- commit hash: be9c7cb
- commit date: 2026-05-01
- overall geometric mean: 1.022x faster
- HPT reliability: 61.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 239 ms: 2.18x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.9 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 58.0 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 888 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.67 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 785 us: 2.60x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 239 ms: 2.18x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| pylint                           | 106 ms                                                         | 51.8 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 504 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 612 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.9 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 812 ns: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.6 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 888 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.05x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 337 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 689 ms: 1.06x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 43.6 ns: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.3 ms: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 344 us: 1.11x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.67 ms: 1.12x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.23 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.6 us: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.13 us: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.0 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.28x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                    |
| many_optionals                   | 200 us                                                         | 261 us: 1.30x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 44.7 ms: 1.33x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 58.0 ms: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 61.1 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.9 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260501-3.15.0a8+-be9c7cb-NOGIL/bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 61.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x