# Results vs. 3.13.0rc2

- fork: python
- ref: bde12919522b0c40fd9e
- machine: darwin-arm64
- commit hash: bde1291
- commit date: 2025-09-05
- overall geometric mean: 1.009x faster
- HPT reliability: 66.26%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 982 ms: 1.07x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.49 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.89 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| mako            | 4.41 ms                                                        | 5.76 ms: 1.31x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 758 us: 2.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 472 us: 2.11x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 602 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| deepcopy                         | 145 us                                                         | 116 us: 1.25x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 62.1 ms: 1.17x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| docutils                         | 1.05 sec                                                       | 982 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| fannkuch                         | 179 ms                                                         | 187 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 341 ms: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 694 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.49 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.49 us: 1.12x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.5 ns: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.7 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.78 us: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.4 us: 1.14x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.2 ms: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.89 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.2 ms: 1.17x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.42 us: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.8 ms: 1.27x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.29 ms: 1.29x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.76 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.1 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 591 us: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 334 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.5 ms: 2.95x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): sphinx, json, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250905-3.15.0a0-bde1291-NOGIL/bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 66.26% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x