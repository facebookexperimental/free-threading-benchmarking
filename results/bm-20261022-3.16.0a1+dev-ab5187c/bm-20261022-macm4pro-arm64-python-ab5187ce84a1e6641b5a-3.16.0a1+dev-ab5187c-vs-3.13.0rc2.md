# Results vs. 3.13.0rc2

- fork: python
- ref: ab5187ce84a1e6641b5a
- machine: darwin-arm64
- commit hash: ab5187c
- commit date: 2026-10-22
- overall geometric mean: 1.112x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.00x faster                                                        |
| docutils       | 1.05 sec                                                       | 898 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| sphinx         | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 261 ms: 2.01x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 274 ms: 1.90x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 276 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                        |
| async_generators                 | 193 ms                                                         | 140 ms: 1.38x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.84 ms: 1.09x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.4 ms: 3.16x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                       |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                        |
| nbody          | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.5 ms: 1.06x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.49 ms: 1.33x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 807 ms: 1.24x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.7 ms: 1.10x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 93.0 us: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.2 us: 1.06x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.23 ms: 1.05x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 497 ms: 2.13x faster                                                        |
| pylint                           | 106 ms                                                         | 51.5 ms: 2.05x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 261 ms: 2.01x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 274 ms: 1.90x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.87 ms: 1.62x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 619 us: 1.60x faster                                                        |
| deepcopy                         | 145 us                                                         | 94.6 us: 1.53x faster                                                       |
| k_core                           | 1.46 sec                                                       | 967 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 276 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                       |
| go                               | 72.6 ms                                                        | 51.3 ms: 1.42x faster                                                       |
| async_generators                 | 193 ms                                                         | 140 ms: 1.38x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 48.1 us: 1.34x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.49 ms: 1.33x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.1 ms: 1.33x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 807 ms: 1.24x faster                                                        |
| pyflate                          | 222 ms                                                         | 179 ms: 1.24x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.23x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.73 ms: 1.18x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                       |
| float                            | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                       |
| docutils                         | 1.05 sec                                                       | 898 ms: 1.17x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                      |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.7 ms: 1.12x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 111 ms: 1.12x faster                                                        |
| fannkuch                         | 179 ms                                                         | 161 ms: 1.11x faster                                                        |
| richards                         | 22.1 ms                                                        | 19.9 ms: 1.11x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.7 ms: 1.10x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.59 ms: 1.10x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.84 ms: 1.09x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 40.7 ms: 1.07x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.8 ms: 1.07x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 93.0 us: 1.07x faster                                                       |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                       |
| sphinx                           | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.2 us: 1.06x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 89.5 ms: 1.06x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.12 us: 1.05x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.23 ms: 1.05x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 308 ms: 1.05x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 907 ns: 1.04x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.21 ms: 1.04x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.60 us: 1.03x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 632 ms: 1.03x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.75 ms: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                        |
| pycparser                        | 470 ms                                                         | 466 ms: 1.01x faster                                                        |
| 2to3                             | 112 ms                                                         | 111 ms: 1.00x faster                                                        |
| chaos                            | 24.3 ms                                                        | 24.2 ms: 1.00x faster                                                       |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                        |
| nbody                            | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 97.3 ms: 1.02x slower                                                       |
| raytrace                         | 109 ms                                                         | 111 ms: 1.02x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 53.9 ms: 1.03x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 44.7 ms: 1.04x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                        |
| generators                       | 15.7 ms                                                        | 16.8 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.1 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                       |
| many_optionals                   | 200 us                                                         | 219 us: 1.09x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.9 ms: 1.13x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.4 ms: 3.16x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (4): meteor_contest, mako, connected_components, logging_silent
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261022-3.16.0a1+dev-ab5187c/bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x