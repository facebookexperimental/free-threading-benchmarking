# Results vs. 3.13.0rc2

- fork: python
- ref: ffaec6e2a11fb7b41fac
- machine: darwin-arm64
- commit hash: ffaec6e
- commit date: 2025-08-27
- overall geometric mean: 1.022x faster
- HPT reliability: 86.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.87 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.4 ms: 2.99x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.4 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.4 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 923 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.1 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 535 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| go                               | 72.6 ms                                                        | 55.5 ms: 1.31x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.27x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.4 ms: 1.27x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.87 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 923 ms: 1.08x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 952 us: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.4 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.0 ms: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.1 us: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.51 ms: 1.00x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 659 ms: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.4 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.29 us: 1.02x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.51 us: 1.03x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.6 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.4 ms: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.6 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.94 ms: 1.09x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.43 us: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.3 ms: 1.15x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 319 us: 1.59x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.74x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.4 ms: 2.99x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (7): pathlib, logging_silent, regex_compile, genshi_xml, thrift, sphinx, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 86.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x