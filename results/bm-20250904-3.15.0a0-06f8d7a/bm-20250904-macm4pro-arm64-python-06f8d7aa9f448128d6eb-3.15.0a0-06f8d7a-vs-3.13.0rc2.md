# Results vs. 3.13.0rc2

- fork: python
- ref: 06f8d7aa9f448128d6eb
- machine: darwin-arm64
- commit hash: 06f8d7a
- commit date: 2025-09-04
- overall geometric mean: 1.016x faster
- HPT reliability: 65.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.4 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 925 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.3 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.9 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.5 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.8 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| mdp                              | 1.06 sec                                                       | 548 ms: 1.93x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 957 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.28x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.77 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 925 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 943 us: 1.05x faster                                                    |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.3 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.1 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.4 us: 1.02x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 40.1 ns: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.3 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.9 us: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.0 ms: 1.00x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.56 ms: 1.00x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.87 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.5 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 956 ns: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 326 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 664 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.8 ms: 1.05x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 497 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 51.0 ms: 1.07x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.1 ms: 1.09x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.52 us: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.4 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 320 us: 1.60x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.3 ms: 2.76x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (2): genshi_text, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 65.44% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x