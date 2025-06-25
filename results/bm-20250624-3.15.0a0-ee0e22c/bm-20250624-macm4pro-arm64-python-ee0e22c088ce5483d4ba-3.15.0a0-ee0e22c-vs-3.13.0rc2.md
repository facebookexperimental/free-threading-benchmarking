# Results vs. 3.13.0rc2

- fork: python
- ref: ee0e22c088ce5483d4ba
- machine: darwin-arm64
- commit hash: ee0e22c
- commit date: 2025-06-24
- overall geometric mean: 1.019x faster
- HPT reliability: 58.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 926 ms: 1.08x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.5 ms: 1.00x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 518 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 947 ms: 1.55x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.29x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.28x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| go                               | 72.6 ms                                                        | 57.7 ms: 1.26x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.0 ms: 1.26x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 926 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 947 us: 1.05x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.2 us: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| float                            | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.48 ms: 1.01x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.83 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.5 ms: 1.00x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 25.1 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.0 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 969 ns: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.7 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 339 ms: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 686 ms: 1.06x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                   |
| pycparser                        | 470 ms                                                         | 504 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.6 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.41 us: 1.09x slower                                                   |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.8 ms: 1.11x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.60 us: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.4 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.75 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 199 ns: 4.90x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (6): json, async_tree_eager, pathlib, async_tree_eager_cpu_io_mixed, xml_etree_generate, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 58.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x