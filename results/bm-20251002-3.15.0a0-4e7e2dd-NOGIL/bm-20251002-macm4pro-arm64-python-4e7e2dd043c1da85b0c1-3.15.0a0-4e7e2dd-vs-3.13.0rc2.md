# Results vs. 3.13.0rc2

- fork: python
- ref: 4e7e2dd043c1da85b0c1
- machine: darwin-arm64
- commit hash: 4e7e2dd
- commit date: 2025-10-02
- overall geometric mean: 1.005x faster
- HPT reliability: 68.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 986 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.7 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.1 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.8 ms: 1.25x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.04 ms: 1.15x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 971 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.93 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                   |
| mako            | 4.41 ms                                                        | 5.80 ms: 1.32x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 764 us: 2.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 481 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.82x faster                                                    |
| mdp                              | 1.06 sec                                                       | 608 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.7 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.8 ms: 1.25x faster                                                   |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 62.3 ms: 1.17x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.04 ms: 1.15x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.6 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 828 ns: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| docutils                         | 1.05 sec                                                       | 986 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 971 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.11 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 338 us: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.9 ns: 1.10x slower                                                   |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 361 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.5 ms: 1.12x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 731 ms: 1.13x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.2 ms: 1.14x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.6 ms: 1.16x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 74.8 us: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.93 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.2 ms: 1.19x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.42 us: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.26 ms: 1.27x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.7 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.80 ms: 1.32x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.1 ms: 1.32x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.9 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 552 us: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 341 us: 1.70x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 19.2 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (2): pycparser, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 68.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x