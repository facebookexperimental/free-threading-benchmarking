# Results vs. 3.13.0rc2

- fork: python
- ref: 6dad8b88cc39d8f9f41c
- machine: darwin-arm64
- commit hash: 6dad8b8
- commit date: 2026-09-18
- overall geometric mean: 1.055x faster
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 946 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 339 ms: 1.55x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 338 ms: 1.54x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 326 ms: 1.24x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 339 ms: 1.14x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.46 ms: 1.14x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 133 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 247 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 262 ms: 1.26x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.0 ms: 1.48x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.54x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| nbody          | 42.5 ms                                                        | 41.2 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.37 ms: 1.18x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 53.9 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 828 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.5 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 94.2 us: 1.06x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 66.7 ms: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.25 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 509 ms: 2.08x faster                                                    |
| pylint                           | 106 ms                                                         | 56.0 ms: 1.89x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 339 ms: 1.55x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.06 ms: 1.54x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 338 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 984 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.6 us: 1.46x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                   |
| go                               | 72.6 ms                                                        | 52.0 ms: 1.39x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 47.5 ms: 1.35x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 48.9 us: 1.32x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 326 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 828 ms: 1.21x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 833 us: 1.19x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.37 ms: 1.18x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 339 ms: 1.14x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.46 ms: 1.14x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.9 ms: 1.11x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 112 ms: 1.11x faster                                                    |
| docutils                         | 1.05 sec                                                       | 946 ms: 1.11x faster                                                    |
| fannkuch                         | 179 ms                                                         | 162 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.5 ms: 1.09x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 34.6 ms: 1.08x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 302 ms: 1.06x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 94.2 us: 1.06x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 41.8 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.96 ms: 1.04x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 624 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                    |
| nbody                            | 42.5 ms                                                        | 41.2 ms: 1.03x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.60 us: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 924 ns: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.42 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.3 ns: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| bench_thread_pool                | 412 us                                                         | 414 us: 1.00x slower                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.8 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.3 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.0 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.7 ms: 1.07x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.25 ms: 1.07x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 133 ms: 1.09x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.7 ms: 1.09x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 247 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.9 ms: 1.12x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                   |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.4 ms: 1.23x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 262 ms: 1.26x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.0 ms: 1.48x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.54x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (2): async_tree_memoization, json_loads
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 99.78% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x