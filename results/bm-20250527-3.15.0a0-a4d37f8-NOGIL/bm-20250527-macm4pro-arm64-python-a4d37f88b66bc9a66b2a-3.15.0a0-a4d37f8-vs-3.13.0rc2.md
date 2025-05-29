# Results vs. 3.13.0rc2

- fork: python
- ref: a4d37f88b66bc9a66b2a
- machine: darwin-arm64
- commit hash: a4d37f8
- commit date: 2025-05-27
- overall geometric mean: 1.030x faster
- HPT reliability: 55.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 189 ms: 2.75x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.88x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.7 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.08x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.2 ms: 2.63x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.27x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 53.7 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.13 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 956 ms: 1.05x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.4 us: 1.15x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.40 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.86 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                   |
| mako            | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                   |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 189 ms: 2.75x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 761 us: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 475 us: 2.09x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 553 ms: 1.91x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.88x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.7 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                    |
| go                               | 72.6 ms                                                        | 59.2 ms: 1.23x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.5 us: 1.22x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.13 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.5 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.08x faster                                                   |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.23 us: 1.06x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 956 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.96 ms: 1.04x slower                                                   |
| json                             | 1.94 ms                                                        | 2.02 ms: 1.04x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.90 ms: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.25 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| thrift                           | 309 us                                                         | 329 us: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.5 ms: 1.09x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.40 ms: 1.09x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.0 us: 1.11x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.66 us: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.6 ms: 1.14x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.4 us: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.86 ms: 1.15x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 372 ms: 1.15x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 184 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.6 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 757 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.0 ms: 1.20x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 41.4 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.76 us: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.05 us: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                   |
| nbody                            | 42.5 ms                                                        | 53.7 ms: 1.26x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 591 us: 1.44x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.53 ms: 1.52x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 69.1 ms: 1.62x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.2 ms: 2.63x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 214 ns: 5.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): regex_dna, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250527-3.15.0a0-a4d37f8-NOGIL/bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 55.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x