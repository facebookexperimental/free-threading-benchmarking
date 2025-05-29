# Results vs. 3.13.0rc2

- fork: python
- ref: a4d37f88b66bc9a66b2a
- machine: darwin-arm64
- commit hash: a4d37f8
- commit date: 2025-05-27
- overall geometric mean: 1.028x faster
- HPT reliability: 97.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 403 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.1 ms: 3.05x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.5 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.60 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 902 ms: 1.11x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.45 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.3 us: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.58 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| mdp                              | 1.06 sec                                                       | 512 ms: 2.07x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 951 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| go                               | 72.6 ms                                                        | 56.0 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.9 ms: 1.28x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.60 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 902 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| float                            | 31.4 ms                                                        | 29.5 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 947 us: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.45 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.7 us: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.36 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.3 us: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.01x faster                                                   |
| sphinx                           | 409 ms                                                         | 403 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| meteor_contest                   | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.58 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 957 ns: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.7 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.6 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.6 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.3 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.46 us: 1.10x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 354 ms: 1.10x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 717 ms: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.2 ms: 1.10x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.27 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.76 us: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.65 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.1 ms: 3.05x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 198 ns: 4.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): genshi_xml, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250527-3.15.0a0-a4d37f8/bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 97.71% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x