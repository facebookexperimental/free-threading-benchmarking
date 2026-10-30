# Results vs. 3.13.0rc2

- fork: python
- ref: ef1fce0a69a19360643f
- machine: darwin-arm64
- commit hash: ef1fce0
- commit date: 2026-10-29
- overall geometric mean: 1.112x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| docutils       | 1.05 sec                                                       | 898 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| sphinx         | 409 ms                                                         | 385 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 263 ms: 1.99x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.3 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 268 ms: 1.44x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.78 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                       |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| nbody          | 42.5 ms                                                        | 43.8 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.00 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.0 ms: 1.06x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 792 ms: 1.26x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.8 us: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.19 ms: 1.05x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.45 ms: 1.01x slower                                                       |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 497 ms: 2.13x faster                                                        |
| pylint                           | 106 ms                                                         | 50.2 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 263 ms: 1.99x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.3 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.87x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 619 us: 1.60x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.95 ms: 1.59x faster                                                       |
| deepcopy                         | 145 us                                                         | 95.0 us: 1.53x faster                                                       |
| k_core                           | 1.46 sec                                                       | 972 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 268 ms: 1.44x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                       |
| go                               | 72.6 ms                                                        | 51.2 ms: 1.42x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 46.0 us: 1.41x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.3 ms: 1.32x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.26x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 792 ms: 1.26x faster                                                        |
| pyflate                          | 222 ms                                                         | 179 ms: 1.24x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.00 ms: 1.19x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.74 ms: 1.17x faster                                                       |
| docutils                         | 1.05 sec                                                       | 898 ms: 1.17x faster                                                        |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.16x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.8 ms: 1.11x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                        |
| richards                         | 22.1 ms                                                        | 19.9 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.78 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.61 ms: 1.09x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 115 ms: 1.08x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 34.7 ms: 1.07x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 92.8 us: 1.07x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.06x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 89.0 ms: 1.06x faster                                                       |
| sphinx                           | 409 ms                                                         | 385 ms: 1.06x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.3 ms: 1.06x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.19 ms: 1.05x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 907 ns: 1.04x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.21 ms: 1.04x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.35 us: 1.04x faster                                                       |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| pprint_pformat                   | 650 ms                                                         | 629 ms: 1.03x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.59 us: 1.03x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                       |
| thrift                           | 309 us                                                         | 301 us: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                        |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.01x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 410 us: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.01x faster                                                        |
| meteor_contest                   | 47.9 ms                                                        | 48.1 ms: 1.01x slower                                                       |
| chaos                            | 24.3 ms                                                        | 24.5 ms: 1.01x slower                                                       |
| mako                             | 4.41 ms                                                        | 4.45 ms: 1.01x slower                                                       |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 97.6 ms: 1.02x slower                                                       |
| nbody                            | 42.5 ms                                                        | 43.8 ms: 1.03x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 54.1 ms: 1.03x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.08x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.5 ms: 1.09x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.6 ms: 1.09x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                       |
| many_optionals                   | 200 us                                                         | 226 us: 1.13x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 42.9 ms: 1.13x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (1): logging_silent
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261029-3.16.0a1+dev-ef1fce0/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x