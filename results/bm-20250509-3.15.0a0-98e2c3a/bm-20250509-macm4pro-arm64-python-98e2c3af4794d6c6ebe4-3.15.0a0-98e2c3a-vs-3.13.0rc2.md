# Results vs. 3.13.0rc2

- fork: python
- ref: 98e2c3af4794d6c6ebe4
- machine: darwin-arm64
- commit hash: 98e2c3a
- commit date: 2025-05-09
- overall geometric mean: 1.008x faster
- HPT reliability: 65.44%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 26.4 ms: 1.14x slower                                                   |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 260 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.58x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.7 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 51.4 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.58 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 951 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.5 ms: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| json_dumps           | 4.65 ms                                                        | 5.18 ms: 1.11x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.51 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.09 ms: 1.02x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.04x slower                                                   |
| mako            | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 260 ms: 2.00x faster                                                    |
| mdp                              | 1.06 sec                                                       | 537 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.58x faster                                                    |
| k_core                           | 1.46 sec                                                       | 959 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.31x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                   |
| go                               | 72.6 ms                                                        | 57.4 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 52.4 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 930 us: 1.07x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 951 ms: 1.05x faster                                                    |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.5 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| float                            | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.58 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.51 ms: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.84 ms: 1.00x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.1 ms: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.2 ms: 1.01x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.0 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 659 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.09 ms: 1.02x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.03x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.04x slower                                                   |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 67.2 us: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.1 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 437 us: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 51.0 ms: 1.07x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.08x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 47.4 ms: 1.08x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 5.18 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.9 ms: 1.14x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 26.4 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.9 ms: 1.14x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.04 ms: 1.14x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.88 us: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.86 us: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| nbody                            | 42.5 ms                                                        | 51.4 ms: 1.21x slower                                                   |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.65 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.7 ms: 3.07x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 196 ns: 4.83x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (3): async_tree_eager, coroutines, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-98e2c3a/bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 65.44% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x