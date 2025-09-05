# Results vs. 3.13.0rc2

- fork: python
- ref: fc0305a2d8bef7cffaa4
- machine: darwin-arm64
- commit hash: fc0305a
- commit date: 2025-09-04
- overall geometric mean: 1.021x faster
- HPT reliability: 89.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.3 ms: 1.00x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.4 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.2 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 915 ms: 1.09x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.3 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 541 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| go                               | 72.6 ms                                                        | 56.8 ms: 1.28x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 915 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 932 us: 1.07x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.3 ms: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| float                            | 31.4 ms                                                        | 31.3 ms: 1.00x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 959 ns: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.2 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 671 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.54 us: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.06x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 497 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.2 ms: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.5 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.95 ms: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.47 us: 1.10x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.4 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.2 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 316 us: 1.58x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.75x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (8): spectral_norm, fannkuch, scimark_monte_carlo, thrift, genshi_text, sphinx, json, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 89.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x