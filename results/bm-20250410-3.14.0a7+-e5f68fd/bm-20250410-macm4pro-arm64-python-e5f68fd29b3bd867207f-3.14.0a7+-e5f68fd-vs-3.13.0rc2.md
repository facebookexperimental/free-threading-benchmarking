# Results vs. 3.13.0rc2

- fork: python
- ref: e5f68fd29b3bd867207f
- machine: darwin-arm64
- commit hash: e5f68fd
- commit date: 2025-04-10
- overall geometric mean: 1.036x faster
- HPT reliability: 93.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                    |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.4 ms: 3.05x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.9 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 885 ms: 1.13x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 99.2 us: 1.00x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.11 ms: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.5 ms: 1.00x slower                                                    |
| mako            | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                     |
| mdp                              | 1.06 sec                                                       | 520 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| k_core                           | 1.46 sec                                                       | 940 ms: 1.56x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.4 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 877 us: 1.13x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 885 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.95 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.9 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.5 us: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 932 ns: 1.02x faster                                                     |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.01 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.1 ns: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.2 us: 1.00x faster                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.5 ms: 1.00x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.5 ms: 1.00x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.5 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 655 ms: 1.01x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 24.9 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                     |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 98.4 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.04x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.6 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.33 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.4 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 439 us: 1.07x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.5 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.46 us: 1.10x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.11 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 233 us: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.70 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.4 ms: 3.05x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (2): richards, pprint_safe_repr
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250410-3.14.0a7+-e5f68fd/bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 93.46% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x