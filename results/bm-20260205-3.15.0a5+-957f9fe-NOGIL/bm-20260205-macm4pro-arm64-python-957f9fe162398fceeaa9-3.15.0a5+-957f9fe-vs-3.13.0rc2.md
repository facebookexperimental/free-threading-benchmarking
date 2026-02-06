# Results vs. 3.13.0rc2

- fork: python
- ref: 957f9fe162398fceeaa9
- machine: darwin-arm64
- commit hash: 957f9fe
- commit date: 2026-02-05
- overall geometric mean: 1.040x faster
- HPT reliability: 81.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 967 ms: 1.08x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 237 ms: 2.20x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 238 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.3 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.9 ms: 3.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 8.96 ms: 1.19x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 90.6 ms: 1.04x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 759 us: 2.69x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 237 ms: 2.20x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 491 us: 2.02x faster                                                     |
| mdp                              | 1.06 sec                                                       | 586 ms: 1.80x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 238 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 103 us: 1.41x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 58.6 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 777 ns: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.21x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 8.96 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.1 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| docutils                         | 1.05 sec                                                       | 967 ms: 1.08x faster                                                     |
| pidigits                         | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 90.6 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 454 ms: 1.04x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.4 ms: 1.02x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.02x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.03x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 676 ms: 1.04x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 25.8 ms: 1.04x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.3 ms: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.90 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| thrift                           | 309 us                                                         | 328 us: 1.06x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 70.1 us: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.1 ns: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 59.4 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 183 ms: 1.15x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.8 ms: 1.16x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.14 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.19 us: 1.20x slower                                                    |
| coverage                         | 31.2 ms                                                        | 37.6 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.26x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.7 ms: 1.28x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.2 ms: 1.29x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 547 us: 1.33x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.9 ms: 3.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260205-3.15.0a5+-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 81.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x