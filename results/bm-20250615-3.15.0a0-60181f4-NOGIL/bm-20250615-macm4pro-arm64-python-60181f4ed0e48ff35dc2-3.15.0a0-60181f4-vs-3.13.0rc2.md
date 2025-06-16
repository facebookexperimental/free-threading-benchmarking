# Results vs. 3.13.0rc2

- fork: python
- ref: 60181f4ed0e48ff35dc2
- machine: darwin-arm64
- commit hash: 60181f4
- commit date: 2025-06-15
- overall geometric mean: 1.008x faster
- HPT reliability: 85.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): tomli_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                   |
| mako            | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 800 us: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 494 us: 2.01x faster                                                    |
| mdp                              | 1.06 sec                                                       | 569 ms: 1.86x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                   |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 61.6 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 826 ns: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| float                            | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.23 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| thrift                           | 309 us                                                         | 329 us: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.4 ms: 1.10x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.2 ms: 1.11x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.8 ms: 1.12x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.7 us: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.3 ms: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.68 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.95 us: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 379 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 771 ms: 1.19x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.84 us: 1.27x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.13 us: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.8 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 595 us: 1.44x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 65.8 ms: 1.54x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.71 ms: 1.55x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 215 ns: 5.30x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): tomli_loads, json_dumps
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250615-3.15.0a0-60181f4-NOGIL/bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 85.75% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x