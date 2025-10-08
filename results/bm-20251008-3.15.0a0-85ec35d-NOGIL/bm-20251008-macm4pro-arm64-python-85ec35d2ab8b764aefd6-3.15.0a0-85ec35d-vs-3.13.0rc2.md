# Results vs. 3.13.0rc2

- fork: python
- ref: 85ec35d2ab8b764aefd6
- machine: darwin-arm64
- commit hash: 85ec35d
- commit date: 2025-10-08
- overall geometric mean: 1.003x slower
- HPT reliability: 80.34%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.0 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.7 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.3 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.09 ms: 1.14x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.9 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.60 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| mako            | 4.41 ms                                                        | 5.84 ms: 1.32x slower                                                   |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 782 us: 2.61x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 490 us: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                                    |
| mdp                              | 1.06 sec                                                       | 601 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.0 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 995 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.24x faster                                                   |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                   |
| go                               | 72.6 ms                                                        | 62.4 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.5 ms: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 833 ns: 1.14x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.09 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                   |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.3 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.04x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.08 ms: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.9 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 355 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.0 ns: 1.11x slower                                                   |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.60 ms: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 724 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.5 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.9 us: 1.14x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.85 us: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.4 ms: 1.17x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.0 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.7 ms: 1.22x slower                                                   |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.5 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.51 us: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.4 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.1 ms: 1.32x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.84 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 558 us: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.7 ms: 1.36x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 66.6 ms: 1.56x slower                                                   |
| many_optionals                   | 200 us                                                         | 346 us: 1.72x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 19.4 ms: 3.11x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 80.34% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x