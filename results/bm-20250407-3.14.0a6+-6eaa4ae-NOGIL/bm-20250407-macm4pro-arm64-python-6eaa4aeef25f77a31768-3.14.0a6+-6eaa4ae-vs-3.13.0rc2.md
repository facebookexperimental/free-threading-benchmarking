# Results vs. 3.13.0rc2

- fork: python
- ref: 6eaa4aeef25f77a31768
- machine: darwin-arm64
- commit hash: 6eaa4ae
- commit date: 2025-04-07
- overall geometric mean: 1.030x faster
- HPT reliability: 52.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 982 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.58x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.8 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 229 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 221 ms: 1.06x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 53.2 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 35.2 ms: 1.31x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 54.9 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 946 ms: 1.06x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.42 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.50 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                    |
| mako            | 4.41 ms                                                        | 5.42 ms: 1.23x slower                                                    |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 732 us: 2.79x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.58x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 444 us: 2.24x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.07x faster                                                     |
| mdp                              | 1.06 sec                                                       | 563 ms: 1.88x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.8 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 229 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 35.2 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                     |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 812 ns: 1.17x faster                                                     |
| go                               | 72.6 ms                                                        | 62.5 ms: 1.16x faster                                                    |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 54.9 ms: 1.14x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.5 us: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| docutils                         | 1.05 sec                                                       | 982 ms: 1.07x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 946 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 231 ms: 1.03x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.19 ms: 1.04x slower                                                    |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.93 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 221 ms: 1.06x slower                                                     |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 40.9 ms: 1.08x slower                                                    |
| fannkuch                         | 179 ms                                                         | 194 ms: 1.08x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.42 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 717 ms: 1.10x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.2 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.0 us: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.12x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.51 us: 1.12x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.63 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 59.6 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.16x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.6 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.10 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 47.9 ns: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                     |
| many_optionals                   | 200 us                                                         | 237 us: 1.18x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 40.3 ms: 1.20x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.42 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.5 ms: 1.25x slower                                                    |
| nbody                            | 42.5 ms                                                        | 53.2 ms: 1.25x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.53 us: 1.25x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.50 ms: 1.26x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.74 ms: 1.40x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 577 us: 1.40x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): json, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250407-3.14.0a6+-6eaa4ae-NOGIL/bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 52.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x