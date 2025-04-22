# Results vs. 3.13.0rc2

- fork: python
- ref: 3cfab449ab1e3c1472d2
- machine: darwin-arm64
- commit hash: 3cfab44
- commit date: 2025-04-21
- overall geometric mean: 1.020x faster
- HPT reliability: 54.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.3 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.4 ms: 1.03x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 99.4 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 927 ms: 1.08x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.00 ms: 1.07x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.97 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                     |
| mdp                              | 1.06 sec                                                       | 517 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                     |
| k_core                           | 1.46 sec                                                       | 943 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.9 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 58.9 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 882 us: 1.13x faster                                                     |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 927 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                     |
| float                            | 31.4 ms                                                        | 30.4 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.82 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 938 ns: 1.01x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.4 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.3 ms: 1.02x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.6 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.4 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.2 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.97 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                     |
| fannkuch                         | 179 ms                                                         | 187 ms: 1.05x slower                                                     |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.4 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 40.5 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 441 us: 1.07x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.00 ms: 1.07x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.66 us: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.43 us: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.45 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.99 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 48.1 ms: 1.13x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.75 us: 1.14x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 240 us: 1.20x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.88 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.3 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (5): typing_runtime_protocols, scimark_monte_carlo, sphinx, async_tree_eager, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250421-3.14.0a7+-3cfab44/bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 54.58% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x