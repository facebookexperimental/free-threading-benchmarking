# Results vs. 3.13.0rc2

- fork: python
- ref: 78cfee6f0920ac914ed1
- machine: darwin-arm64
- commit hash: 78cfee6
- commit date: 2025-04-20
- overall geometric mean: 1.034x faster
- HPT reliability: 54.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 979 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 412 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.0 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.85 ms: 1.09x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.0 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 52.6 ms: 1.24x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.82 ms: 1.09x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.8 ms: 1.05x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.8 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.6 ms: 1.07x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 941 ms: 1.06x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.3 ms: 1.04x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.1 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| mako            | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                                    |
| django_template | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 751 us: 2.72x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 443 us: 2.24x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                     |
| mdp                              | 1.06 sec                                                       | 558 ms: 1.90x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.0 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 977 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 60.2 ms: 1.20x faster                                                    |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.3 ms: 1.18x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 806 ns: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 14.7 us: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.85 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.82 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.09x faster                                                    |
| docutils                         | 1.05 sec                                                       | 979 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.6 ms: 1.07x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 941 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 457 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| sphinx                           | 409 ms                                                         | 412 ms: 1.01x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                    |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.3 ms: 1.04x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.82 ms: 1.04x slower                                                    |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                     |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                     |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 99.8 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.28 ms: 1.07x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.0 ms: 1.07x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.06 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.57 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.8 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 354 ms: 1.10x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.7 ms: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.1 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 720 ms: 1.11x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 71.7 us: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.49 us: 1.12x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.0 ms: 1.12x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.1 us: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.76 us: 1.13x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.66 ms: 1.13x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.2 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.0 ms: 1.15x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 46.8 ns: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.0 ms: 1.16x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.16x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 40.2 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.37 us: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                                    |
| nbody                            | 42.5 ms                                                        | 52.6 ms: 1.24x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.1 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.38x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.78 ms: 1.40x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250420-3.14.0a7+-78cfee6-NOGIL/bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 54.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.17x