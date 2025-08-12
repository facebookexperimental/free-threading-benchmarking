# Results vs. 3.13.0rc2

- fork: python
- ref: dd079db4b96fa474b8e6
- machine: darwin-arm64
- commit hash: dd079db
- commit date: 2025-08-12
- overall geometric mean: 1.001x slower
- HPT reliability: 85.07%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.3 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 1.02 sec: 1.02x slower                                                  |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.1 ms: 1.13x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                   |
| mako            | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 779 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 487 us: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                    |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 62.3 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 831 ns: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| float                            | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.02 sec: 1.02x slower                                                  |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.3 ms: 1.03x slower                                                   |
| json                             | 1.94 ms                                                        | 2.02 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.26 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.9 ns: 1.11x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                   |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 726 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.1 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.56 us: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 74.0 us: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.85 us: 1.17x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.8 ms: 1.18x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 113 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 57.2 ms: 1.19x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.3 ms: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.9 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.46 us: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.27 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.7 ms: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.4 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                    |
| many_optionals                   | 200 us                                                         | 333 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.3 ms: 2.93x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250812-3.15.0a0-dd079db-NOGIL/bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 85.07% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x