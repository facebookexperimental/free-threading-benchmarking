# Results vs. 3.13.0rc2

- fork: python
- ref: 483d130e504f63aaf3af
- machine: darwin-arm64
- commit hash: 483d130
- commit date: 2025-05-04
- overall geometric mean: 1.035x faster
- HPT reliability: 93.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 108 ms: 1.03x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 25.6 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.99 ms: 1.07x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 99.8 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 945 ms: 1.06x faster                                                     |
| unpickle_pure_python | 99.5 us                                                        | 97.9 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.00 ms: 1.07x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.05 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| mdp                              | 1.06 sec                                                       | 518 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| go                               | 72.6 ms                                                        | 56.1 ms: 1.29x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 51.2 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.16x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 869 us: 1.14x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.4 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                     |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.99 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 945 ms: 1.06x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| 2to3                             | 112 ms                                                         | 108 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.33 ms: 1.03x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.99 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.9 us: 1.02x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.7 ms: 1.02x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.1 ns: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 938 ns: 1.01x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 324 ms: 1.01x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 65.2 us: 1.01x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.0 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.05 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.3 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                     |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 39.7 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.8 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 435 us: 1.06x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                     |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.00 ms: 1.07x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 47.1 ms: 1.08x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.40 ms: 1.08x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 25.6 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.97 ms: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.59 us: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                    |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 9.16 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (8): sphinx, json, pathlib, pprint_pformat, fannkuch, deltablue, genshi_xml, xml_etree_process
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250504-3.14.0a7+-483d130/bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 93.78% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x