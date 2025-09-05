# Results vs. 3.13.0rc2

- fork: python
- ref: fc0305a2d8bef7cffaa4
- machine: darwin-arm64
- commit hash: fc0305a
- commit date: 2025-09-04
- overall geometric mean: 1.001x slower
- HPT reliability: 76.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| docutils       | 1.05 sec                                                       | 993 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.4 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.04 ms: 1.15x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.56 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| mako            | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 769 us: 2.65x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 477 us: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 617 ms: 1.71x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.4 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1000 ms: 1.46x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.27x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| go                               | 72.6 ms                                                        | 62.7 ms: 1.16x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.04 ms: 1.15x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 56.0 ms: 1.14x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 833 ns: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 203 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| docutils                         | 1.05 sec                                                       | 993 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.04x slower                                                    |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.09x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 354 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.56 ms: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 721 ms: 1.11x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.2 ns: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                   |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 74.2 us: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.0 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 146 ms: 1.18x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.7 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.19x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.3 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.21x slower                                                    |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.7 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.51 us: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.2 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.33 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.1 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 591 us: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 337 us: 1.68x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): pycparser, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 76.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x